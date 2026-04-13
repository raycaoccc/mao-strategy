# Self-Criticism Review (批评与自我批评)

Sources:《论联合政府》(On Coalition Government, 1945),《关于纠正党内的错误思想》(On Correcting Mistaken Ideas, 1929),《整顿党的作风》(Rectify the Party's Style of Work, 1942)

---

## Principle (原理)

**批评与自我批评** — Criticism and self-criticism is the method for identifying and correcting errors through honest, structured review where each participant examines their own failings before offering feedback to others.

Core concepts:

- **自我批评为先 (Self-criticism first)**: Before criticizing others, honestly examine one's own contribution to the problem. This creates psychological safety and sets the standard of honesty.
- **惩前毖后，治病救人 (Learn from past mistakes to prevent future ones; treat the illness to save the patient)**: The goal is improvement, not punishment. Criticism must be constructive, specific, and forward-looking.
- **团结—批评—团结 (Unity → Criticism → Unity)**: Start from a desire for unity, conduct criticism honestly, achieve a new and higher-level unity. The process strengthens relationships rather than damaging them.
- **实事求是 (Seek truth from facts)**: Criticism must be based on observed facts, not impressions, rumors, or personality judgments.
- **对事不对人 (Address the matter, not the person)**: Critique decisions and actions, not character or intentions.

**Key insight**: Organizations that lack a structured mechanism for honest self-assessment repeat mistakes indefinitely. Self-criticism is the immune system.

---

## When to Apply

- After a project failure, incident, or missed deadline
- After a project success (to capture what worked and why)
- Periodic team health checks (quarterly or after major milestones)
- When the same problems keep recurring
- When team trust or communication has degraded
- Before starting a new phase of work (reviewing the previous phase)

---

## How to Apply (Step-by-Step)

### Step 1: Set the Frame — Unity First (团结)

Before any criticism begins, establish:
- **Shared goal**: "We are all here because we want [project/team] to succeed"
- **Ground rules**: Facts, not feelings. Actions, not character. Forward-looking, not backward-blaming.
- **Scope**: Define what period, project, or incident is being reviewed
- **Safety**: Honest self-assessment will be valued, not punished

If the team lacks trust for open discussion, start with written anonymous submissions and discuss themes rather than attributing specific feedback.

### Step 2: Self-Criticism Round (自我批评)

Each participant answers honestly:

1. **What was my responsibility in this situation?**
2. **What did I do that contributed to the problem?**
3. **What did I fail to do that I should have?**
4. **What assumptions did I hold that turned out to be wrong?**
5. **What will I do differently next time?**

**Rules for self-criticism**:
- Be specific: "I did not review the migration plan before approving it" not "I should have been more careful"
- Be honest: do not use self-criticism as false modesty or as a way to pre-empt others' feedback
- Be actionable: every criticism must pair with a concrete change

**The leader goes first.** This sets the standard and demonstrates that self-criticism applies at all levels.

### Step 3: Constructive Criticism Round (批评)

After self-criticism, participants offer feedback to others:

**Structure each piece of criticism as**:
1. **Observation** (fact): "During the deploy, the rollback plan was not tested"
2. **Impact** (consequence): "This meant that when the deploy failed, rollback took 4 hours instead of 15 minutes"
3. **Suggestion** (forward-looking): "For future deploys, I propose we add rollback testing to the pre-deploy checklist"

**Rules for criticism**:
- 对事不对人 — address the action, not the person
- 实事求是 — base criticism on observed facts, not impressions
- Be specific and actionable
- Acknowledge what went well alongside what did not
- One issue at a time — do not pile on

### Step 4: Synthesize Lessons (综合总结)

After both rounds, synthesize:

| Category | Content |
|----------|---------|
| **What went well** | Practices to continue and reinforce |
| **What went wrong** | Root causes identified (not just symptoms) |
| **What was learned** | New understanding gained |
| **Action items** | Concrete, assigned, time-bound changes |
| **Systemic issues** | Problems that require structural fixes, not just individual behavior changes |

### Step 5: Close with Unity (团结)

End the session by:
- Acknowledging the courage of honest self-assessment
- Confirming action items and owners
- Reaffirming the shared goal
- Scheduling follow-up to verify action items were completed

**The cycle is**: Unity (we share a goal) → Criticism (we honestly assess) → Unity (we are stronger for having done so).

### Step 6: Follow Up

A review without follow-through is worse than no review — it teaches the team that reviews are theater.

- Track action items to completion
- At the next review, start by checking whether previous action items were implemented
- If an action item was not implemented, that becomes the first item for discussion

---

## Modern Example

**Scenario**: A product launch missed its deadline by 3 weeks and shipped with a critical bug that required a hotfix on day one.

**Frame setting**: "We are here to learn from this launch so the next one goes better. This is not about blame — it is about improving our process."

**Self-criticism round**:
- **Product manager**: "I changed the feature scope twice in the last month before launch. This created rework and uncertainty about what 'done' looked like. Next time I will freeze scope 4 weeks before launch."
- **Tech lead**: "I knew the test coverage was thin but I did not escalate because I thought we could handle it. Next time I will flag test coverage gaps as launch blockers, not risks."
- **Engineering manager**: "I did not push back on the deadline when scope changed. I treated the original date as fixed even though the requirements moved. Next time I will renegotiate the deadline when scope changes significantly."

**Criticism round**:
- Engineer → Tech lead: "The architecture decision to use the new queue system was made without a spike. It worked in staging but failed under production load. Suggestion: require a load-test spike for new infrastructure components before launch."
- Tech lead → PM: "The second scope change was communicated in a Slack thread, not a spec update. Three engineers missed it. Suggestion: all scope changes go through the spec document with explicit changelog."

**Synthesis**:
- What went well: Team rallied for the hotfix; customer communication was excellent
- Root causes: scope instability + insufficient testing + new infra without load testing
- Action items:
  1. [PM, by next sprint] Create scope freeze policy: no changes within 4 weeks of launch
  2. [Tech lead, by next sprint] Add test coverage threshold to launch checklist
  3. [Eng manager, ongoing] Renegotiate deadlines when scope changes >10%
  4. [Team, by next quarter] Add load-test requirement for new infrastructure components

**Follow-up**: At the next monthly engineering review, check whether these 4 items were implemented. Start there before discussing new topics.
