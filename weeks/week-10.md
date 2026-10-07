# Week 10: Evaluation and Observability

**Syllabus:** Module 8 (part 1) | **Phase:** Production | **Project:** Production Observability Pipeline

## Why this matters (PM lens)
"Does it work?" is not answerable by trying it twice. Evals are the **acceptance criteria** of agent products, and you, as the PM, should own them. Observability tells you what went wrong, how slow it was and what it cost.

## Concepts in plain English
- **Eval set:** a fixed list of test inputs with expected qualities. Run it after every change, like regression tests.
- **Metrics (Ragas / TruLens):**
  - *Faithfulness:* does the answer stick to the retrieved sources?
  - *Answer relevance:* does it actually address the question?
  - *Context precision/recall:* did retrieval find the right passages?
  - *Factual grounding:* can each claim be traced to a source?
- **LLM-as-judge:** using a model to score outputs. Useful but needs spot-checking by humans.
- **Tracing:** a timeline of every step: prompts, tool calls, responses, errors (**LangSmith**, **AgentOps**).
- **Latency diagnostics:** which step is slow?
- **Cost tracking:** tokens in, tokens out, cost per task and per user. Know your unit economics.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Build an eval set of 30 questions for your week 6/7 RAG bot, with human-checked reference answers |
| 2 (2h) | Run Ragas or TruLens on it. Read the scores and examine low-scoring cases by hand |
| 3 (2h) | Connect LangSmith or AgentOps to your agent. Browse traces |
| Weekend (4h) | Make one improvement driven by evals, then show the metric moving. Build the deliverable |

## Deliverable: Production Observability Pipeline
`projects/week10/observability/`:
- An existing agent (RAG bot or planner) instrumented with traces
- A dashboard or screenshots showing: a full trace, the slowest step, cost per task
- Eval report: baseline scores, one change made (e.g. better chunking), after scores
- A one-page **"quality and cost" brief** a stakeholder could read: target metrics, current metrics, cost per 1,000 tasks

## Check yourself
- What does a faithfulness score of 0.6 tell you?
- Why can't you only trust an LLM judge?
- Which trace view helps you find why a task took 40 seconds?
- What's the cost per task of your agent, and what would make it 3x cheaper?

## Stretch
Write a pass/fail threshold on your eval set and run it automatically before any change (a preview of week 11 CI).
