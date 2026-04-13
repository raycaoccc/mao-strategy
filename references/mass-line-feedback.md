# Mass Line Feedback (群众路线)

Sources:《关于领导方法的若干问题》(Some Questions Concerning Methods of Leadership, 1943),《论联合政府》(On Coalition Government, 1945)

---

## Principle (原理)

**从群众中来，到群众中去** — From the masses, to the masses.

Sound decisions emerge from a cycle: gather scattered, unprocessed ideas from the people closest to the problem; synthesize them into systematic, coherent plans; bring those plans back to the people for testing and validation; iterate.

Core concepts:

- **集中起来 (Concentrate)**: Raw input from many sources is scattered and often contradictory. The leader's job is to distill it into a coherent direction — not to follow every voice, but to find the pattern.
- **坚持下去 (Persist through iteration)**: One round of gathering-and-synthesizing is not enough. Each cycle refines the plan through real-world feedback.
- **一般与个别相结合 (Combine the general with the particular)**: General principles must be adapted to specific situations. Feedback from specific cases tests and sharpens general plans.
- **领导与群众相结合 (Combine leadership with the masses)**: Neither top-down directives nor bottom-up anarchy alone produces good outcomes. The synthesis of both is required.
- **民主性与参与性 (Democratic participation)**: The mass line is inherently democratic — it requires genuine, not performative, participation. The people closest to the problem must have real voice in shaping the solution, not merely be consulted for appearances.

**Key insight**: The best plans emerge not from a single brilliant mind, but from the disciplined cycle of genuinely democratic listening, rigorous synthesizing, and iterative testing with the people who will execute and be affected by the plan.

---

## When to Apply

- Making decisions that affect many stakeholders
- Building team alignment around a direction
- Product decisions that require user buy-in
- Setting strategy when the team holds diverse opinions
- When top-down decisions have failed to get traction
- When bottom-up suggestions feel contradictory or unfocused
- Any situation where execution depends on buy-in from the people executing

---

## How to Apply (Step-by-Step)

### Step 1: Gather Input Broadly (从群众中来)

Collect perspectives from the people closest to the problem:

| Method | Best For | Watch Out For |
|--------|----------|---------------|
| 1-on-1 conversations | Honest, detailed input; sensitive topics | Time-intensive; may miss group dynamics |
| Group brainstorm | Breadth of ideas; energy | Groupthink; loudest voice dominates |
| Written submissions | Thoughtful, considered input; introverts | Low response rate if not structured |
| Data/metrics review | Objective evidence; scale | Misses qualitative context |
| Observation | Actual behavior vs stated preferences | Observer effect; interpretation bias |

**Critical rule**: Gather from the actual people affected, not only from their managers or representatives. 眼睛向下 — look downward to the front line.

### Step 2: Synthesize into a Coherent Proposal (集中起来)

Raw input is scattered. Synthesize it:

1. **Group by theme**: What are the 3-5 major themes that emerge?
2. **Identify tensions**: Where do perspectives conflict? (Use Contradiction Analysis if complex)
3. **Find the signal**: What do most people agree on, even if they frame it differently?
4. **Draft a proposal**: Formulate a plan that addresses the major themes and resolves the key tensions
5. **Be explicit about trade-offs**: State what the proposal prioritizes and what it deprioritizes, and why

The synthesis must be more than a summary — it must be a decision with clear rationale.

### Step 3: Return to the People for Validation (到群众中去)

Present the synthesized plan back to stakeholders:

- Share the proposal with the **same people** who provided input
- Explicitly show how their input influenced the plan
- Ask targeted questions: "Does this capture the core of what you raised? What did we get wrong?"
- Listen for: resistance (may indicate missed concerns), confusion (may indicate unclear communication), enthusiasm (may indicate alignment)

### Step 4: Iterate Based on Feedback

Incorporate feedback and repeat:

- **Round 1**: Broad input → initial synthesis → validation
- **Round 2**: Refined input (now focused on specific concerns) → adjusted plan → re-validation
- **Round 3** (if needed): Final adjustments → commitment

Most decisions need 2 rounds. Complex or high-stakes decisions may need 3. More than 3 rounds indicates either insufficient synthesis or genuinely irreconcilable positions (at which point, decide and move forward).

### Step 5: Execute with Continued Feedback

Implementation is not the end of the feedback loop:

- Build feedback channels into the execution plan
- Schedule check-ins at meaningful milestones
- Be willing to adjust the plan based on execution-phase learning
- Close the loop: tell people what changed because of their feedback

---

## Modern Example

**Scenario**: An engineering director needs to decide on a new code review process after the current one receives widespread complaints.

**Round 1 — Gather input**:
- 1-on-1s with 6 engineers across different teams: "What is broken about code review? What would your ideal process look like?"
- Survey to all 30 engineers: 3 targeted questions about pain points
- Metrics: average review turnaround time (48 hours), review-related blockers per sprint (3.2)
- Raw themes: reviews take too long; reviewers lack context; too many nitpick comments; no clear ownership

**Round 1 — Synthesize**:
- Principal tension: thoroughness vs speed
- Proposal: Introduce "review tiers" — small changes get lightweight review (< 4 hours SLA), large changes get full review (< 24 hours SLA). Assign primary reviewer based on code ownership. Separate style checks to automated linting.

**Round 1 — Validate**:
- Present proposal in team meeting. Engineers agree on tiering but raise concern: "Who decides what's small vs large?" Suggestion: use diff size + file ownership as automatic classifier.

**Round 2 — Refine**:
- Add automatic classification rules. Refine SLAs based on feedback. Address edge case: cross-team changes always get full review.
- Re-validate: Engineers sign off. Pilot for 2 sprints.

**Execution feedback**:
- After 2 sprints: review turnaround dropped to 18 hours. Blockers dropped to 1.4 per sprint. One team reports the classifier misses some complex-but-small changes. Adjust classifier to include "files touched across 3+ modules" as a trigger for full review.

**Result**: A process that works because the people executing it shaped it.
