# Contradiction Analysis (矛盾论 + 抓主要矛盾)

Sources:《矛盾论》(On Contradiction, 1937),《关于正确处理人民内部矛盾的问题》(On the Correct Handling of Contradictions Among the People, 1957)

---

## Principle (原理)

Every situation, system, or project contains multiple **contradictions** (矛盾) — tensions between opposing forces. These contradictions are not bugs; they are the fundamental structure of how things develop and change.

Core concepts:

- **矛盾的普遍性 (Universality of contradiction)**: Contradictions exist in everything. A project without apparent tensions is one where tensions have not been identified yet.
- **矛盾的特殊性 (Particularity of contradiction)**: Each situation's contradictions are unique. Do not apply generic templates — analyze the specific case.
- **主要矛盾 (Principal contradiction)**: Among all contradictions, one is dominant. Resolving it often simplifies or resolves the secondary ones.
- **矛盾的主要方面 (Principal aspect)**: Within each contradiction, one side is dominant and determines the nature of the tension.
- **矛盾的同一性与斗争性 (Unity and struggle of opposites)**: The two aspects of every contradiction are both opposed (struggle) and interdependent (unity). They coexist within the same entity and can transform into each other under certain conditions. Understanding this duality prevents treating contradictions as simple either/or choices.
- **矛盾的转化 (Transformation of contradictions)**: Principal and secondary can swap positions as conditions change. What was secondary yesterday may become principal today. The dominant aspect within a contradiction can also flip — this is how qualitative change occurs.

**Key Quotes (引用语录)**:

> "在复杂的事物的发展过程中，有许多的矛盾存在，其中必有一种是主要的矛盾，由于它的存在和发展，规定或影响着其他矛盾的存在和发展。" ——《矛盾论》

> "捉住了这个主要矛盾，一切问题就迎刃而解了。" ——《矛盾论》

> "不同质的矛盾，只有用不同质的方法才能解决。" ——《矛盾论》

> "对于矛盾的各种不平衡情况的研究，对于主要的矛盾和非主要的矛盾、主要的矛盾方面和非主要的矛盾方面的研究，成为革命政党正确地决定其政治上和军事上的战略战术方针的重要方法之一。" ——《矛盾论》

**Key insight**: Seize the principal contradiction to focus effort, but remember that contradictions are dynamic and interconnected — resolving the principal contradiction reshapes the entire field, it does not mechanically eliminate all problems.

---

## When to Apply

- Multiple competing priorities with no clear order
- Team disagreements about what matters most
- Root cause unclear among many symptoms
- Resources insufficient to address everything simultaneously
- After a change in conditions that may have shifted priorities

---

## How to Apply (Step-by-Step)

### Step 1: Enumerate All Contradictions

List every tension, trade-off, or conflict in the situation. Be exhaustive. Common categories:

| Category | Example Tensions |
|----------|-----------------|
| Resource | Speed vs quality; cost vs capability |
| Stakeholder | User needs vs business goals; team A vs team B priorities |
| Technical | Scalability vs simplicity; innovation vs stability |
| Temporal | Short-term wins vs long-term investment |
| Organizational | Autonomy vs alignment; speed vs process |

### Step 2: Identify the Two Aspects of Each Contradiction

For each contradiction, name the two opposing forces and assess:
- Which aspect is currently **dominant** (主要方面)?
- Which aspect is currently **subordinate** (次要方面)?

Example: "Speed vs quality" — currently speed is dominant (team ships fast but with bugs).

### Step 3: Determine the Principal Contradiction (主要矛盾)

Ask: **"If I could resolve only ONE tension, which one would most change the overall situation?"**

Tests for identifying the principal contradiction:
- Resolving it would reduce or eliminate several secondary contradictions
- It is the bottleneck that other problems depend on
- Stakeholders with the most influence care most about this one
- Ignoring it will worsen the overall situation regardless of other progress

### Step 4: Analyze the Principal Contradiction Deeply

For the principal contradiction:
- What caused it to become principal?
- What conditions would cause it to transform (主次矛盾转化)?
- What is the principal aspect — which side has leverage?
- What would resolution look like?

### Step 5: Allocate Effort

- **Primary effort** (70-80% of resources): Address the principal contradiction
- **Maintenance effort** (20-30%): Keep secondary contradictions from escalating
- **Monitoring**: Watch for signs of transformation — secondary contradictions becoming principal

### Step 6: Re-evaluate Periodically

After significant progress or changed conditions, repeat from Step 1. The principal contradiction shifts — what was secondary may now be principal. This is normal and expected.

---

## Modern Example

**Scenario**: A startup has four tensions:
1. **Product quality vs speed to market** — users report bugs, but competitors are gaining ground
2. **Technical debt vs new features** — codebase is fragile, but users demand features
3. **Team burnout vs delivery pressure** — engineers are exhausted, but deadlines are firm
4. **Customer acquisition vs retention** — new users arrive, but churn is high

**Analysis**:
- Enumerate: 4 contradictions listed above
- Aspects: Speed is dominant in #1; features dominant in #2; delivery pressure dominant in #3; acquisition dominant in #4
- **Principal contradiction**: #4 (acquisition vs retention). High churn makes acquisition futile — a leaky bucket. If retention improves, acquisition ROI improves, pressure eases, and quality focus becomes viable.
- Principal aspect: Acquisition is dominant but retention is the lever. Shift resources to retention.
- Effort allocation: 70% on retention (fix top churn drivers), 20% on maintaining acquisition pipeline, 10% on monitoring #3 (burnout could escalate)
- Re-evaluate: After one quarter, churn data will reveal if #4 is resolving and whether #2 (tech debt) has become the new principal contradiction
