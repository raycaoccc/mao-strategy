# Worked Example: Should We Migrate from Monolith to Microservices?

This example demonstrates the full 5-step consultation workflow applied to a technical architecture decision.

---

## Situation

A mid-size e-commerce company (80 engineers, $50M revenue) has a 7-year-old Rails monolith that handles everything: user management, product catalog, orders, payments, search, and recommendations. The monolith deploys once per day; deploy failures cause 2-3 hours of downtime per month. Three teams work in the same codebase and frequently block each other with merge conflicts. The VP of Engineering proposes a 12-month migration to microservices. The CTO is skeptical — the last partial migration attempt (2 years ago) failed after 4 months and was abandoned.

---

## Step 1: Describe the Situation (描述情况)

- **Problem**: Monolith is creating development velocity and reliability issues
- **Proposed action**: Full microservices migration over 12 months
- **Stakeholders**:
  - VP Engineering: champions migration, believes microservices will unblock teams
  - CTO: skeptical due to previous failure; worried about complexity
  - 3 engineering teams (25+ each): frustrated with merge conflicts and slow deploys
  - Product team: wants faster feature delivery; does not care about architecture
  - Ops team (5 people): manages deployment; overwhelmed with current infra
  - Business: revenue growing 30% YoY; cannot afford extended instability
- **Constraints**: Cannot stop feature development during migration; ops team already at capacity; previous migration attempt failed; revenue growth must continue
- **Desired outcome**: Faster, independent team deployments with fewer incidents

---

## Step 2: Identify Contradictions (识别矛盾)

| # | Contradiction | Dominant Aspect |
|---|--------------|----------------|
| 1 | **Migration ambition vs previous failure** — want to move forward vs fear of repeating history | Fear is dominant (failure is fresh memory) |
| 2 | **Development velocity vs migration overhead** — need speed now vs investing for future speed | Velocity need is dominant (business growing 30%) |
| 3 | **Team autonomy vs shared codebase** — teams want independence vs single repo coupling | Coupling is dominant (daily merge conflicts) |
| 4 | **Ops capacity vs infrastructure complexity** — 5-person ops team vs potential 10+ services | Capacity constraint is dominant |
| 5 | **Full migration vs incremental improvement** — big bet vs small steps | Full migration is currently proposed |

**Principal contradiction (主要矛盾)**: **#3 — Team autonomy vs shared codebase coupling**. This is the root cause of the velocity and reliability issues. Merge conflicts, slow deploys, and cross-team blocking all stem from this coupling. Resolving it does not require full microservices — it requires decoupling.

**Principal aspect**: Coupling is dominant. The teams are forced into shared-codebase patterns that create daily friction. The lever is decoupling, not necessarily microservices.

**矛盾的特殊性 (Particularity)**: This situation's coupling problem is specific — 3 teams, 6 domains, 1 repo. The solution must address this specific topology, not follow generic "microservices good, monolith bad" advice.

---

## Step 3: Select Frameworks (选择框架)

1. **Practice-Theory Cycle (实践论)** — primary. The previous migration failed. The team must learn from that failure before attempting again. Theory (microservices will help) must be validated through practice (incremental extraction).
2. **Protracted Strategy (论持久战)** — secondary. This is a multi-year architectural evolution, not a 12-month project. Phase the approach.
3. **Self-Criticism Review (批评与自我批评)** — prerequisite. Before planning the new migration, honestly review why the previous one failed.

---

## Step 4: Apply Analysis (应用分析)

### Self-Criticism Review Application (prerequisite)

Before planning forward, review the failed migration from 2 years ago.

**Questions for the team**:
- What was attempted? (Which service was extracted? What was the scope?)
- Why did it fail? (Technical reasons? Organizational? Scope?)
- What did each leader contribute to the failure?
- What would we do differently?

**Likely findings** (hypothetical but common):
- Attempted to extract the most complex domain first (payments) instead of the simplest
- Did not invest in shared infrastructure (service mesh, monitoring) before extraction
- Underestimated data migration complexity
- Did not reduce feature work during migration — tried to do both at full speed

**Lesson**: 战术上重视 — tactically, treat each step with full seriousness. The previous attempt was strategically correct (decoupling is needed) but tactically careless (wrong starting point, no infrastructure foundation, no scope protection).

### Practice-Theory Cycle Application

**Current theory**: "Microservices will solve our coupling problems"

**问题**: This theory has not been tested in this organization. The previous failure suggests the theory may be incomplete — microservices might solve coupling but introduce operational complexity that the 5-person ops team cannot handle.

**Proposed cycle**:

**Cycle 1 — Test the decoupling theory without microservices**:
- Theory: Team coupling can be reduced within the monolith through module boundaries
- Practice: Introduce strict module boundaries in the monolith (separate directories, defined interfaces, no cross-module database queries). Deploy this for 2 months.
- Expected perception: Merge conflicts decrease; teams gain partial independence
- Verification: Measure merge conflict rate and cross-team blocking incidents

**Cycle 2 — Test operational readiness for services**:
- Theory: The ops team can handle a second deployable unit
- Practice: Extract the simplest, most independent domain (e.g., search or recommendations) into a separate service. Run it for 3 months.
- Expected perception: Learn the real operational cost of running a second service
- Verification: Ops incident rate, deploy frequency, team satisfaction

**Cycle 3 — Decide on expansion**:
- If Cycles 1-2 succeed: Extract next domain. Continue incrementally.
- If Cycle 1 succeeds but Cycle 2 fails: Invest in ops infrastructure before extracting more.
- If Cycle 1 fails: The problem is not architecture — it is team process. Reconsider.

### Protracted Strategy Application

**Phase assessment**: Strategic defensive. The monolith is working (revenue growing 30%). The team does not need to "win the war" immediately — it needs to build capability for future independence without risking current stability.

**Phased plan**:

| Phase | Duration | Focus | Success Metric |
|-------|----------|-------|---------------|
| **Defensive** (modularize monolith) | 3 months | Strict module boundaries, CI enforcement, reduced coupling | Merge conflicts down 50% |
| **Stalemate** (first extraction) | 6 months | Extract 1 simple service, build shared infra (monitoring, deploy pipeline) | Second service running in production with < 0.1% error rate |
| **Early offensive** (expand) | 6-12 months | Extract 1-2 more domains based on learnings | 3+ independently deployable units, each team owns their deploy |
| **Full offensive** | 12+ months | Only if validated — continue extraction for remaining domains | Teams deploy independently, < 1 hour downtime per month |

**集中优势兵力**: Do not extract all 6 domains simultaneously. Concentrate the best engineers on one extraction at a time. Win each battle decisively before starting the next.

---

## Step 5: Propose Action (提出行动)

### Immediate Actions (This Week)
1. **Conduct self-criticism review**: Half-day session with VP Eng, CTO, and team leads reviewing the previous migration failure
2. **Reframe the proposal**: From "12-month microservices migration" to "incremental decoupling validated through practice"
3. **Identify the simplest domain**: Likely search or recommendations — least coupled, most independent

### Short-Term Actions (This Month)
4. **Start Cycle 1**: Introduce module boundaries in the monolith; enforce via linting and CI
5. **Invest in monitoring**: Before extracting anything, ensure the team can observe a distributed system (tracing, centralized logging, health checks)
6. **Scope protect**: Reserve 20% of engineering capacity for decoupling work; 80% continues feature development

### Long-Term Direction (This Quarter+)
7. **Cycle 2 at month 3**: Extract first service if module boundaries are validated
8. **Phase gate at month 6**: Full review — is the approach working? Adjust or continue
9. **No commitment to full microservices**: Each extraction is evaluated independently. Stop extracting if the cost exceeds the benefit.

### Review Checkpoints
- **Month 1**: Module boundaries in place; merge conflict metrics
- **Month 3**: First service extracted; ops team assessment
- **Month 6**: Phase gate — continue, pause, or change approach
- **Month 12**: Strategy review — how many services, what benefit, what cost

### Risks
- Principal contradiction may shift: if modularizing the monolith solves 80% of the coupling pain, full microservices may not be needed (this is a good outcome, not a failure)
- Ops team bottleneck becomes the new principal contradiction after first extraction → address by investing in platform engineering before further extractions
- Business pressure accelerates timeline → 战略上藐视，战术上重视 — remain confident in the long-term direction but refuse to rush tactical steps that will fail
