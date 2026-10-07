# Week 2: Python for AI: Types, Async, APIs, Retries

**Syllabus:** Module 1 (Validation, async, API resilience, data frameworks) | **Phase:** Foundations

## Why this matters (PM lens)
LLM outputs are messy and APIs fail. Production agents are mostly about **validating data, being fast, and surviving failure**. These skills are the difference between a demo and a product.

## Concepts in plain English
- **Type hints:** labelling what kind of data a function expects (`age: int`). Helps you and tools catch mistakes.
- **Pydantic:** turns those labels into enforced rules. If an LLM returns `"age": "banana"`, Pydantic rejects it before it breaks your app.
- **Async / `asyncio`:** while waiting for one slow API call, start others. Ten calls take about 1 call's time instead of 10x.
- **Calling web APIs:** send a request, get JSON back. Includes API keys (never put them in code; use environment variables or a `.env` file).
- **Retries with backoff:** if a call fails, wait 1s, then 2s, then 4s before giving up.
- **Logging levels:** DEBUG, INFO, WARNING, ERROR. You will rely on logs to understand agent behavior.
- **Pandas / Polars:** spreadsheets in code. Only the basics: load, filter, group, summarize.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Type hints and Pydantic models. Validate good and bad JSON |
| 2 (2h) | Call a public API (weather, jokes, anything free). Parse the response into a Pydantic model |
| 3 (2h) | Async: fetch 10 URLs one by one, then in parallel with `asyncio`, and compare timing |
| Weekend (4h) | Retries, error handling, logging. Pandas basics (1h). Build the deliverable |

## Deliverable
`projects/week02/resilient_fetcher/`:
- Takes a list of 20 API requests
- Runs them in parallel
- Validates every response with Pydantic
- Retries failures with backoff
- Writes INFO and ERROR logs to a file
- Prints a Pandas summary: successes, failures, average time

Deliberately make 3 requests fail and show the system recovers.

## Check yourself
- Why validate LLM output even when it "looks right"?
- When is async faster, and when does it not help?
- What's the risk of retrying with no limit or delay?
- Why must API keys stay out of your code and your Git history?

## Stretch
Re-do the summary with Polars and compare how it feels.
