# Capstone Project

A week-long, end-to-end build: an agentic system for a realistic business use case. You pick it in week 8 and build it in week 12 (with 1-2 hours of prep in weeks 9-11).

## The four parts (from the syllabus)

| Part | What it means | Evidence |
|---|---|---|
| **Blueprint** | Break a complex problem into autonomous sub-tasks | Architecture diagram, list of agents/tools/data |
| **Engine** | State machine, planning loops, robust error recovery | State diagram, 3 handled failure cases |
| **Guardrails** | Metrics for grounding (Ragas/TruLens) and prompt-injection defense | Eval report, red-team table |
| **Ship** | Production-ready Docker container | `docker run` works; CI file; README |

## Idea menu (pick one, or propose your own)

| Idea | Why it's a good fit |
|---|---|
| **Automated market research:** given a company or product, collect public info, compare competitors, write a brief with citations | Planning + RAG + multi-agent, and PM-relevant |
| **PRD reviewer:** reads a product requirements doc and returns gaps, risks, unclear requirements and test questions | Uses your domain knowledge; easy to evaluate yourself |
| **Customer feedback analyzer:** ingests reviews or tickets, clusters themes, drafts a prioritized insights report | Data processing + crew + clear value |
| **Automated code review pipeline** | Matches the syllabus example, but harder for non-engineers |
| **Support triage agent:** classify, retrieve policy, draft a reply, escalate when unsure, with memory of the customer | Hits memory, RAG, guardrails |

**Choose by:** (1) you understand the domain, (2) you can get or make 30+ realistic test cases, (3) a failure is not dangerous, (4) it needs at least a planning loop and 3 tools.

## Proposal template (1 page, due end of week 8)

1. **Problem and user:** who has it, what it costs them today
2. **What the agent does** (3 sentences) and what it won't do
3. **Sub-tasks and agents/tools**
4. **Data sources** and how you'll get test data
5. **How I'll know it works:** 3 metrics with target numbers (e.g. faithfulness above 0.85; under $0.30 per task; under 60 seconds)
6. **Top 3 risks** (including one security risk)
7. **Cut list:** what I'll drop if time runs short

## Grading rubric (self-assessment, 100 points)

| Area | Points | Strong looks like |
|---|---|---|
| Problem and design | 15 | Clear user, justified agent design, honest about trade-offs |
| Engine and reliability | 25 | State machine, step limits, recovers from failures |
| Quality evals | 20 | 30+ test cases, metrics tracked, one improvement proven |
| Security and guardrails | 15 | Injection tests with before/after, no secrets leaked, least-privilege tools |
| Observability and cost | 10 | Traces, cost per task, latency known |
| Shipping | 10 | Docker works from a clean start, README, CI |
| Communication | 5 | Demo video and PM brief a stakeholder understands |

**80+** means portfolio-ready. **60-79** means a good prototype; fix the weakest area. **Below 60:** revisit weeks 5, 10 and 11.
