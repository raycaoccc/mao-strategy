---
name: mao-strategy
description: This skill should be used when the user asks to "analyze this decision", "help me think strategically", "what would Mao say", "find the main contradiction", "analyze contradictions", "prioritize competing goals", "stakeholder alignment", "post-mortem analysis", "break down this problem", "strategic analysis", "遇事不决问毛选", "应该怎么办", or needs structured decision-making frameworks derived from Selected Works of Mao Zedong (毛泽东选集). Covers product strategy, technical architecture decisions, organizational change management, team alignment, and retrospective reviews.
version: 0.1.0
tags: [Decision-Making, Strategy, Analysis, Problem-Solving]
author: rayca
created: 2026-04-13
---

# Mao Strategy — 毛选决策框架

Distill decision-making frameworks from《毛泽东选集》(Selected Works of Mao Zedong) into actionable analytical tools for modern problem-solving. This skill extracts **methodology only** — strategic thinking patterns, problem decomposition methods, and decision-making workflows.

Core philosophy: 遇事不决问毛选 — when in doubt, consult the frameworks.

---

## Boundaries

This skill **does**:
- Extract decision-making methodology from《毛泽东选集》
- Apply frameworks to modern technical, product, and organizational problems
- Provide structured analysis with concrete, actionable recommendations

This skill **does not**:
- Provide historical analysis of specific events
- Offer political commentary or ideological advocacy
- Replace domain-specific expertise (engineering, legal, financial)
- Apply to military operations or conflicts (though frameworks use military-derived terminology in abstracted form)

---

## Core Principles (核心原则)

Three foundational ideas run through all frameworks in this skill:

1. **具体问题具体分析 (Concrete analysis of concrete conditions)**: Never apply frameworks mechanically. Every situation is unique. Analyze the specific facts, stakeholders, and constraints of the actual case — generic advice is worthless.

2. **没有调查就没有发言权 (No investigation, no right to speak)**: Decisions must be grounded in firsthand knowledge of actual conditions. Acting on assumptions, secondhand reports, or untested theories produces bad outcomes.

3. **抓主要矛盾 (Seize the principal contradiction)**: Every complex situation contains multiple tensions. Identify the one tension that, if resolved, would most transform the overall situation. Focus effort there; manage the rest with minimal resources.

---

## Consultation Workflow (咨询工作流)

Follow this 5-step process for every consultation. Do not skip steps.

### Step 1: Describe the Situation (描述情况)

State clearly:
- The problem or decision to be made
- Key stakeholders and their positions
- Constraints (time, resources, authority, information)
- Desired outcome and success criteria

If the user's description is vague, ask targeted questions before proceeding. 没有调查就没有发言权 — no investigation, no right to speak.

### Step 2: Identify Contradictions (识别矛盾)

List all tensions, conflicts, and trade-offs in the situation. For each:
- Name the two opposing aspects
- Assess which aspect is currently dominant

Then classify:
- **Principal contradiction (主要矛盾)**: The one tension that, if resolved, would most change the overall situation
- **Secondary contradictions (次要矛盾)**: Important but subordinate tensions

Present this as a structured list. The principal contradiction drives framework selection.

### Step 3: Select Frameworks (选择框架)

Based on the principal contradiction and situation type, select 1-3 frameworks from the index below. Use `references/consultation-decision-tree.md` for detailed routing logic. Typical combinations:

- Complex priority problem → Contradiction Analysis + Investigation Method
- Long-term strategic challenge → Protracted Strategy + Practice-Theory Cycle
- Stakeholder/organizational challenge → United Front + Mass Line
- Post-mortem or review → Self-Criticism + Practice-Theory Cycle

### Step 4: Apply Analysis (应用分析)

Walk through each selected framework's steps against the **concrete situation**. 具体问题具体分析 — concrete analysis of concrete conditions. No abstract theorizing. Every analytical point must reference specific facts from Step 1.

For each framework applied, produce:
- Key insight from the framework
- How it applies to this specific situation
- What action it implies

When multiple frameworks are applied, synthesize their recommendations:
- If frameworks agree, the recommendation is strong — note the convergence.
- If frameworks conflict (e.g., Investigation Method suggests waiting while Protracted Strategy suggests acting), identify which framework addresses the principal contradiction more directly and weight its recommendation accordingly.
- Present the synthesis explicitly: "Framework A suggests X, Framework B suggests Y. Given that the principal contradiction is Z, the recommended path is..."

### Step 5: Propose Action (提出行动)

Synthesize all framework analyses into a unified action plan:
- **Immediate actions** (this week)
- **Short-term actions** (this month)
- **Long-term direction** (this quarter+)
- **Review checkpoints** — when to re-evaluate using 批评与自我批评
- **Risks and contingencies** — what could change the principal contradiction
- **Risk mitigation** — for each major risk, specify a concrete fallback or early warning indicator

---

## Framework Index (框架索引)

### Category 1: Strategic Thinking (战略思维)

| Framework | Chinese | Core Idea | When to Use | Reference |
|-----------|---------|-----------|-------------|-----------|
| Contradiction Analysis | 矛盾论 + 抓主要矛盾 | Every situation has a principal contradiction; solve it first | Multiple competing priorities; unclear root cause | `references/contradiction-analysis.md` |
| Practice-Theory Cycle | 实践论 | Knowledge: practice → theory → practice → verify | Analysis paralysis; theory-practice gap; iterative learning | `references/practice-theory-cycle.md` |
| Protracted Strategy | 论持久战 + 战略战术 | Long contests have phases; match strategy to phase | Multi-year projects; competing against larger opponents | `references/protracted-strategy.md` |

### Category 2: Decision-Making Methods (决策方法)

| Framework | Chinese | Core Idea | When to Use | Reference |
|-----------|---------|-----------|-------------|-----------|
| Investigation Method | 调查研究 | No investigation, no right to speak | Before any major decision; entering unfamiliar territory | `references/investigation-method.md` |
| Mass Line Feedback | 群众路线 | From the masses, synthesize, return to the masses | Team alignment; user-facing decisions; need buy-in | `references/mass-line-feedback.md` |
| United Front | 统一战线 + 星星之火 | Maximize allies, isolate opposition; start small, build momentum | Organizational politics; change management; limited resources | `references/united-front-alliances.md` |

### Category 3: Review & Learning (复盘学习)

| Framework | Chinese | Core Idea | When to Use | Reference |
|-----------|---------|-----------|-------------|-----------|
| Self-Criticism Review | 批评与自我批评 | Honest review: what each party contributed to failure | Post-mortems; retrospectives; periodic health checks | `references/self-criticism-review.md` |

---

## Quick Selection Guide (速查表)

| Problem Pattern | Recommended Framework |
|----------------|----------------------|
| "Too many problems, do not know where to start" | Contradiction Analysis (抓主要矛盾) |
| "Theory and reality do not match" | Practice-Theory Cycle (实践论) |
| "Need allies or facing opposition" | United Front (统一战线) |
| "Long-term goal, unsure about pacing" | Protracted Strategy (论持久战) |
| "Not enough information to decide" | Investigation Method (调查研究) |
| "Need feedback from users or team" | Mass Line Feedback (群众路线) |
| "Something failed, need to learn from it" | Self-Criticism Review (批评与自我批评) |
| "Small resources, big ambition" | United Front — Spark section (星星之火) |
| "Strategic confidence but tactical uncertainty" | Protracted Strategy — strategic contempt + tactical respect (战略上藐视，战术上重视) |

---

## References

- `references/contradiction-analysis.md` — Contradiction theory and principal contradiction identification
- `references/practice-theory-cycle.md` — Theory-practice iteration cycle
- `references/protracted-strategy.md` — Phased strategy and strategic-tactical balance
- `references/investigation-method.md` — Investigation-first decision methodology
- `references/mass-line-feedback.md` — Iterative stakeholder feedback loop
- `references/united-front-alliances.md` — Alliance building and momentum from small beginnings
- `references/self-criticism-review.md` — Structured post-mortem and accountability review
- `references/consultation-decision-tree.md` — Detailed framework selection decision tree
- `examples/example-product-decision.md` — Worked example: product strategy decision
- `examples/example-technical-architecture.md` — Worked example: technical architecture choice
