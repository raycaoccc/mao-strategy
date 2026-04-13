# Investigation Method (调查研究)

Sources:《反对本本主义》(Oppose Book Worship, 1930),《〈农村调查〉的序言和跋》(Preface and Postscript to Rural Surveys, 1941),《关于领导方法的若干问题》(Some Questions Concerning Methods of Leadership, 1943)

---

## Principle (原理)

**没有调查就没有发言权** — No investigation, no right to speak.

Decisions must be grounded in firsthand knowledge of actual conditions, not assumptions, reports of reports, or theoretical deductions. Investigation is not optional preparation — it is the foundation of all sound judgment.

Core concepts:

- **反对本本主义 (Oppose book worship)**: Do not blindly follow frameworks, best practices, or precedent without understanding whether they apply to the current concrete situation.
- **调查就是解决问题 (Investigation is solving the problem)**: The act of thorough investigation often reveals the solution. Many problems persist because no one has looked closely enough.
- **眼睛向下 (Look downward)**: Seek information from the people closest to the problem — front-line workers, end users, the operators — not only from managers or abstractions.
- **详细调查 (Detailed investigation)**: Superficial surveys produce superficial conclusions. Go deep on the critical areas.
- **有目的的调查 (Purposeful investigation)**: Investigation must have clear objectives and direction. Do not investigate everything — focus on what will change the decision. Purposefulness distinguishes strategic investigation from aimless data gathering.

**Key Quotes (引用语录)**:

> "没有调查，没有发言权。" ——《反对本本主义》

> "调查就像'十月怀胎'，解决问题就像'一朝分娩'。调查就是解决问题。" ——《反对本本主义》

> "离开实际调查就要产生唯心的阶级估量和唯心的工作指导，那末，其结果，不是机会主义，便是盲动主义。" ——《反对本本主义》

> "你对于某个问题没有调查，就停止你对于某个问题的发言权。" ——《反对本本主义》

> "中国革命斗争的胜利要靠中国同志了解中国情况。" ——《反对本本主义》

**Key insight**: Most bad decisions result from acting on insufficient or secondhand information. The discipline of purposeful, firsthand investigation prevents this.

---

## When to Apply

- Before any major decision where the team disagrees on facts
- When entering unfamiliar territory (new market, new technology, new team)
- When existing assumptions have not been tested recently
- When someone says "everyone knows that..." without evidence
- When data contradicts conventional wisdom
- As a prerequisite before applying other frameworks — always investigate first

---

## How to Apply (Step-by-Step)

### Step 1: Define What Must Be Known (确定调查目标)

Before investigating, specify:
- What key questions must be answered?
- What information, if obtained, would change the decision?
- What is the minimum viable investigation (given time constraints)?

Avoid open-ended "learn everything" mandates. Focus on decision-critical information.

### Step 2: Go to the Source (深入实际)

Gather firsthand data, not summaries of summaries:

| Information Type | Go-To Source | Avoid |
|-----------------|-------------|-------|
| User behavior | User interviews, usage analytics, support tickets | Internal assumptions about users |
| Technical reality | Read the code, run the system, check logs | Architecture diagrams that may be outdated |
| Market conditions | Customer conversations, competitor analysis | Industry reports alone |
| Team capacity | 1:1 conversations with team members | Manager's estimate of team capacity |
| Process effectiveness | Observe the actual process in action | Process documentation |

**眼睛向下** — Talk to the people doing the work, not only the people managing the work.

### Step 3: Collect Both Quantitative and Qualitative Evidence

- **Quantitative**: Metrics, measurements, counts, timelines, costs
- **Qualitative**: Stories, frustrations, workarounds, wishes, fears

Neither alone is sufficient. Numbers without stories miss context; stories without numbers miss scale.

### Step 4: Distinguish Facts from Interpretations

Maintain strict separation:
- **Fact**: "Response time increased from 200ms to 800ms after the deploy"
- **Interpretation**: "The new service is slow"
- **Root cause** (requires further investigation): Why did response time increase?

Record facts first. Interpret second. Investigate root causes third.

### Step 5: Synthesize Findings (综合分析)

Organize findings into:
- **Confirmed assumptions**: What we believed that turned out to be true
- **Invalidated assumptions**: What we believed that turned out to be false (most valuable)
- **Surprises**: What we did not expect to find
- **Remaining unknowns**: What we still do not know and whether it matters

### Step 6: Form Judgment, Then Act

Only after investigation is complete:
- State conclusions clearly, tied to evidence
- Make recommendations with explicit reasoning
- Identify what further investigation would reveal (diminishing returns assessment)
- Act — investigation without action is wasted effort

---

## Modern Example

**Scenario**: An engineering team is debating whether to adopt Kubernetes for their infrastructure. The CTO read about it at a conference; the senior engineer says it is overkill; the DevOps lead wants it.

**Investigation**:
1. **Define scope**: What must be known? Current infrastructure pain points, team K8s experience, actual scaling requirements, migration cost.
2. **Go to source**: Interview each team member about daily pain points. Review incident logs for the past 6 months. Measure actual traffic patterns and scaling events. Survey the team's container orchestration experience.
3. **Collect evidence**: 
   - Quantitative: 3 scaling incidents in 6 months; current infra handles 95th percentile load; migration estimated at 3 months.
   - Qualitative: DevOps lead spends 30% of time on manual scaling; developers frustrated by deployment complexity; no one on the team has production K8s experience.
4. **Facts vs interpretations**: The fact is 3 scaling incidents. The interpretation "we need K8s" is premature — simpler auto-scaling might solve it.
5. **Synthesis**: Key finding — the real pain is deployment complexity, not scaling. K8s would add scaling capability but increase deployment complexity initially. The principal contradiction is deployment friction, not scale.
6. **Judgment**: Invest in CI/CD pipeline improvements first (addresses principal contradiction). Evaluate K8s in 6 months after team builds container experience. Start with a pilot project, not full migration.
