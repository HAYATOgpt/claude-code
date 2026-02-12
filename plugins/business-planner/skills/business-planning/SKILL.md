---
name: Business Planning
description: This skill should be used when the user asks to "副業を企画する", "ビジネスプランを作る", "事業計画を立てる", "plan a side business", "create a business plan", "副業のアイデアを出す", "収益化の方法を考える", "マネタイズ戦略を考える", "ビジネスモデルを設計する", or wants to brainstorm, evaluate, or structure any business idea or side hustle. Also triggers when the user mentions "副業", "起業", "フリーランス", "収益化", or "monetization" in the context of planning.
version: 0.1.0
---

# Business Planning for AI-Powered Ventures

This skill guides structured business planning through a 5-phase process: Discovery, Analysis, Ideation, Evaluation, and Roadmap. Each phase builds on the previous to produce actionable, personalized business plans rather than generic advice.

## Core Principle

Never generate a business plan without completing the Discovery phase first. Generic plans have no value. The quality of the plan is directly proportional to the depth of situational understanding.

## Phase 1: Discovery (Required)

Gather the user's situation through structured questions. Ask in batches of 2-3 to avoid overwhelming. Cover all six dimensions before proceeding:

### Six Discovery Dimensions

| Dimension | Key Questions | Why It Matters |
|-----------|--------------|----------------|
| **Skills** | Current profession, technical abilities, domain expertise, certifications | Determines what can be offered |
| **Time** | Weekly hours available, schedule flexibility, preferred working hours | Sets realistic scope |
| **Assets** | Existing audience, network, portfolio, equipment, content library | Identifies unfair advantages |
| **Capital** | Initial investment budget, monthly operating budget, risk tolerance | Constrains options |
| **Goals** | Target monthly income, timeline, long-term vision (side income vs. independence) | Shapes strategy |
| **Constraints** | Employment restrictions (non-compete), family obligations, geographic limitations | Eliminates invalid options |

After gathering answers, synthesize into a **Situation Profile** summarizing strengths, gaps, and constraints before moving to Phase 2.

## Phase 2: Situation Analysis

Apply two frameworks to the Discovery findings:

### Skills-Market Matrix

Map the user's skills against market demand:

```
            High Market Demand
                  |
    LEARN TO      |     SWEET SPOT
    MONETIZE      |     (Prioritize)
                  |
  ────────────────┼────────────────
                  |
    AVOID         |     HOBBY
    (Low ROI)     |     (Passion project)
                  |
            Low Market Demand

  Low Skill ←─────────────→ High Skill
```

### AI Leverage Assessment

For each skill, evaluate the AI amplification factor:

- **10x leverage**: AI does 90% of the work (e.g., content generation, code scaffolding)
- **5x leverage**: AI accelerates significantly (e.g., data analysis, research)
- **2x leverage**: AI assists but human expertise dominates (e.g., consulting, coaching)
- **1x leverage**: Minimal AI benefit (e.g., physical services, networking)

Prioritize opportunities where the user has high skill AND high AI leverage.

## Phase 3: Ideation

Generate business ideas using three lenses. Consult `references/ai-business-models.md` for the comprehensive catalog of AI-powered business models with detailed pros/cons and revenue benchmarks.

### Lens 1: Skill Monetization
Transform existing expertise into paid offerings (consulting, courses, services).

### Lens 2: AI Arbitrage
Use AI to deliver services faster/cheaper than competitors (development, content, automation).

### Lens 3: Audience Building
Create free content to build audience, then monetize through products/services.

Generate 5-8 concrete ideas, each with a one-line description and estimated monthly revenue potential.

## Phase 4: Evaluation

Score each idea using the **RIVER Matrix** (consult `references/evaluation-framework.md` for detailed scoring criteria):

| Criterion | Weight | Description |
|-----------|--------|-------------|
| **R**evenue potential | 25% | Realistic monthly income at 3/6/12 months |
| **I**mplementation speed | 20% | Time to first revenue |
| **V**alue alignment | 15% | Match with user's goals and interests |
| **E**ffort sustainability | 20% | Can the user maintain this alongside current commitments? |
| **R**isk level | 20% | Financial risk, reputation risk, dependency risk |

Score each criterion 1-5. Calculate weighted total. Present as a comparison table.

### Decision Output

Recommend the **top 2-3 ideas** with clear reasoning. One should be a "quick win" (fastest to revenue) and one should be the "high ceiling" (highest long-term potential).

## Phase 5: Roadmap

For each recommended idea, create a phased plan. Consult `references/monetization-strategies.md` for platform-specific tactics and pricing strategies.

### Roadmap Structure

**Phase A: Foundation (Week 1-4)**
- Minimum viable offering definition
- Platform/channel setup
- First piece of content or service listing
- Milestone: First public presence

**Phase B: Validation (Month 2-3)**
- First paying customer/sale
- Feedback collection and iteration
- Content/portfolio building
- Milestone: First revenue

**Phase C: Growth (Month 4-6)**
- Optimization based on data
- Second revenue stream introduction
- Audience/network expansion
- Milestone: Target monthly income

Each phase must include:
- Concrete action items with deadlines
- KPIs to track
- Decision criteria for proceeding vs. pivoting
- Estimated time investment per week

## Output Format

Structure the final plan as a Markdown document with:

1. **Situation Profile** (from Discovery)
2. **Skills-Market Analysis** (from Analysis)
3. **Recommended Ideas** (top 2-3 with RIVER scores)
4. **Detailed Roadmap** (for the primary recommendation)
5. **Quick Action List** (what to do this week)
6. **Risk Mitigation** (top 3 risks and countermeasures)

Consult `examples/plan-template.md` for the complete output template.

## Key Rules

- Never skip Discovery. If the user jumps to "give me ideas," redirect to gathering their situation first.
- Always quantify. Replace "you could earn a lot" with specific revenue estimates based on market rates.
- Be honest about downsides. Every business model has weaknesses — surface them early.
- Prefer action over perfection. The plan should be executable this week, not a theoretical exercise.
- Revisit and iterate. Plans improve with real-world feedback. Encourage the user to return after executing Phase A.

## Additional Resources

### Reference Files

For detailed frameworks and data, consult:
- **`references/ai-business-models.md`** - 15+ AI-powered business models with revenue data, pros/cons, and real examples
- **`references/evaluation-framework.md`** - Detailed RIVER scoring criteria and decision matrices
- **`references/monetization-strategies.md`** - Platform-specific monetization tactics, pricing psychology, and scaling strategies

### Example Files

For output formatting:
- **`examples/plan-template.md`** - Complete business plan output template with all sections pre-structured
