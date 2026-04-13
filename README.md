# mao-strategy — 毛选决策框架

Decision-making frameworks distilled from《毛泽东选集》(Selected Works of Mao Zedong) into a [Claude Code](https://claude.ai/claude-code) skill for structured strategic analysis.

遇事不决问毛选 — When in doubt, consult the frameworks.

## What It Does

Provides a **5-step consultation workflow** that applies 7 classical decision-making frameworks to modern technical, product, and organizational problems:

| Framework | Chinese | When to Use |
|-----------|---------|-------------|
| Contradiction Analysis | 矛盾论 + 抓主要矛盾 | Too many competing priorities |
| Investigation Method | 调查研究 | Not enough information to decide |
| Practice-Theory Cycle | 实践论 | Theory and reality don't match |
| Protracted Strategy | 论持久战 | Long-term goal, unsure about pacing |
| Mass Line Feedback | 群众路线 | Need team/user feedback and buy-in |
| United Front | 统一战线 + 星星之火 | Facing opposition or limited resources |
| Self-Criticism Review | 批评与自我批评 | Post-mortem or retrospective |

## Installation

### Option 1: Copy to Claude Code skills directory

```bash
# Clone the repo
git clone https://github.com/raycaoccc/mao-strategy.git

# Copy to your Claude Code skills directory
cp -r mao-strategy ~/.claude/skills/mao-strategy
```

### Option 2: Symlink (recommended for development)

```bash
git clone https://github.com/raycaoccc/mao-strategy.git ~/projects/mao-strategy
ln -s ~/projects/mao-strategy ~/.claude/skills/mao-strategy
```

### Verify Installation

In Claude Code, say any of these to trigger the skill:

- "遇事不决问毛选"
- "help me analyze this decision strategically"
- "find the main contradiction"
- "应该怎么办"

## Usage

Describe your problem or decision, and the skill will guide you through:

1. **Describe the Situation (描述情况)** — Problem, stakeholders, constraints
2. **Identify Contradictions (识别矛盾)** — Find tensions, classify principal vs secondary
3. **Select Frameworks (选择框架)** — Pick 1-3 frameworks based on the principal contradiction
4. **Apply Analysis (应用分析)** — Concrete analysis of concrete conditions
5. **Propose Action (提出行动)** — Phased action plan with review checkpoints

## File Structure

```
mao-strategy/
  SKILL.md                                    # Main skill file (workflow + index)
  references/
    contradiction-analysis.md                 # 矛盾论 + 抓主要矛盾
    practice-theory-cycle.md                  # 实践论
    protracted-strategy.md                    # 论持久战 + 战略战术
    investigation-method.md                   # 调查研究
    mass-line-feedback.md                     # 群众路线
    united-front-alliances.md                 # 统一战线 + 星星之火
    self-criticism-review.md                  # 批评与自我批评
    consultation-decision-tree.md             # Framework selection logic
  examples/
    example-product-decision.md              # Worked example: B2B SaaS pivot
    example-technical-architecture.md        # Worked example: monolith to microservices
```

## Quality

- Reviewed by **Kimi (moonshot-v1-128k)** across 3 rounds: fidelity to source material, practicality, and cross-file coherence
- All source citations verified correct by Kimi
- Scored **A grade (93/100)** by skill-quality-reviewer
- Zero broken file references; all integrity checks pass

## Scope

This skill extracts **methodology only** — strategic thinking patterns and decision-making workflows. It does not provide historical analysis, political commentary, or ideological advocacy.

## License

MIT
