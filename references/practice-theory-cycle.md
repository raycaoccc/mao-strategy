# Practice-Theory Cycle (实践论)

Source:《实践论》(On Practice, 1937)

---

## Principle (原理)

Knowledge develops through an iterative cycle: **practice → perception → theory → practice → verification**. This cycle never ends — each round deepens understanding.

Core concepts:

- **感性认识 (Perceptual knowledge)**: Direct experience produces initial impressions — what is seen, heard, and felt in contact with the actual situation.
- **理性认识 (Rational knowledge)**: Reflection on perceptual experience produces concepts, judgments, and theories — the "why" behind the "what."
- **实践是检验真理的唯一标准 (Practice is the sole criterion for testing truth)**: A theory, no matter how elegant, is not validated until it succeeds in practice.
- **认识的飞跃 (Leap in understanding)**: The jump from perception to theory, and from theory back to practice, are both qualitative leaps that require deliberate effort.
- **认识的反复 (Repetition of knowledge)**: Understanding is not achieved in one pass. It requires multiple cycles, each correcting and deepening the previous one. This is not simple repetition — each cycle operates at a higher level than the last.
- **实践的直接现实性 (Direct reality of practice)**: Practice is the only activity that directly changes objective reality. Theory describes and predicts; practice transforms. This gives practice its unique authority as the criterion of truth — it is not just a test, it is the only test that actually contacts reality.

**Key Quotes (引用语录)**:

> "实践、认识、再实践、再认识，这种形式，循环往复以至无穷，而实践和认识之每一循环的内容，都比较地进到了高一级的程度。" ——《实践论》

> "判定认识或理论之是否真理，不是依主观上觉得如何而定，而是依客观上社会实践的结果如何而定。真理的标准只能是社会的实践。" ——《实践论》

> "通过实践而发现真理，又通过实践而证实真理和发展真理。" ——《实践论》

> "感觉到了的东西，我们不能立刻理解它，只有理解了的东西才更深刻地感觉它。" ——《实践论》

**Key insight**: Neither pure theory nor blind practice alone produces reliable knowledge. Only the disciplined alternation between them does. And when they conflict, practice — as the direct contact with reality — has the final word.

---

## When to Apply

- Analysis paralysis — too much planning, not enough doing
- Reckless execution — too much doing, not enough reflection
- When a team keeps making the same mistakes
- When a well-researched plan fails in implementation
- When an approach "should work in theory" but does not
- At transitions between project phases (prototype → MVP → scale)

---

## How to Apply (Step-by-Step)

### Step 1: Identify Where the Cycle Is Broken

Diagnose which phase is failing:

| Symptom | Broken Phase | Fix |
|---------|-------------|-----|
| "We keep planning but never ship" | Theory → Practice leap missing | Set a deadline for action; accept imperfect plans |
| "We shipped but do not know what we learned" | Practice → Perception missing | Add structured reflection after each iteration |
| "We have data but no insights" | Perception → Theory leap missing | Dedicate time to synthesis and pattern recognition |
| "Our theory was wrong" | Theory → Practice → Verification failing | This is normal — update the theory, do not abandon the process |
| "We keep making the same mistakes" | Full cycle not completing | Institute regular retrospectives tied to action items |

### Step 2: Execute the Current Phase

Based on where the cycle is broken, execute the needed phase:

**If stuck in theory**: Force a small practical experiment. 实践出真知 — true knowledge comes from practice. Define the smallest meaningful test of the theory and execute it.

**If stuck in practice**: Stop and reflect. What patterns have emerged? What has worked and what has not? Distill observations into a working theory (even a tentative one).

**If stuck in perception**: Synthesize. Group observations into categories. Look for causal relationships. Form hypotheses that can be tested.

### Step 3: Make the Leap Deliberate

The transitions between phases do not happen automatically. Schedule them:

- **Practice → Perception**: After each sprint/iteration, schedule a structured debrief
- **Perception → Theory**: After collecting enough observations, schedule a synthesis session
- **Theory → Practice**: Set a deadline — "We will test this hypothesis by [date]"
- **Practice → Verification**: Define success criteria before testing, then measure honestly

### Step 4: Accept Partial Knowledge and Iterate

认识的反复 — understanding comes through repetition. Each cycle produces:
- More accurate perception
- Better-calibrated theory
- More effective practice
- Clearer verification criteria

Do not expect the first cycle to produce definitive answers. Plan for 2-3 iterations minimum on important questions.

### Step 5: Document the Cycle

Record each iteration:
- **What was the theory/plan?** (What did we expect?)
- **What happened in practice?** (What actually occurred?)
- **What was the gap?** (Where did theory and practice diverge?)
- **What is the updated theory?** (What do we now believe?)
- **What will the next practice test?** (How do we verify the update?)

This documentation prevents the team from losing institutional knowledge across iterations.

---

## Modern Example

**Scenario**: A team is building a recommendation engine. Their ML model performs well in offline evaluation but users report irrelevant recommendations.

**Cycle 1**:
- **Theory**: High offline accuracy = good recommendations
- **Practice**: Deploy model, observe user behavior
- **Perception**: Users ignore 70% of recommendations; those they click share a pattern — recency matters more than predicted relevance
- **Gap**: Offline metrics do not capture recency preference
- **Updated theory**: Recommendations must weight recency alongside predicted relevance

**Cycle 2**:
- **Theory**: Adding a recency boost of 0.3 will improve click-through
- **Practice**: A/B test with recency-boosted model
- **Perception**: Click-through improved 15%, but user satisfaction survey shows no change — users click more but do not find content valuable
- **Gap**: Clicks ≠ satisfaction; recency drives curiosity clicks, not value
- **Updated theory**: Need a composite metric (click + dwell time + explicit feedback)

**Cycle 3**:
- **Theory**: Composite metric better captures true recommendation quality
- **Practice**: Retrain with composite objective, A/B test again
- **Verification**: Both click-through (+12%) and satisfaction (+8%) improve
- **Conclusion**: Three cycles were necessary. The first theory was wrong, but each iteration brought the team closer to truth through the discipline of practice → perception → theory → practice.
