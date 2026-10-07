# Week 3: LLMs, Prompting and Context Engineering

**Syllabus:** Module 2 | **Phase:** Foundations | **Project:** Modular Prompt Assembly Lab

## Why this matters (PM lens)
This week changes how you think about software. Traditional software is **deterministic** (same input, same output). LLM systems are **probabilistic**. Your job shifts from specifying exact behavior to **designing conditions that make good behavior likely** and measuring it.

## Concepts in plain English
- **How an LLM works:** it predicts the next token. No database of facts, no true understanding. This explains both its power and hallucinations.
- **Tokens, context windows, temperature:** cost, memory limits, and randomness dials.
- **LLM vs. agent:** a static LLM answers once. An agent plans, uses tools and loops.
- **Prompting techniques:** zero-shot, few-shot, role/system prompts, **Chain-of-Thought**, structured output (JSON).
- **Context engineering:** the real skill. What instructions, examples, documents and history go into the window, in what order, and what gets left out.
- **Model adaptation (concept only):** prompting vs. RAG vs. fine-tuning vs. instruction tuning vs. RLHF. Rule of thumb: try prompting first, then RAG, and fine-tune last.
- **Systems thinking:** probabilistic systems need tests, guardrails and monitoring in place of "it passed once".

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Call an LLM API from Python. Experiment: same prompt 5 times at different temperatures |
| 2 (2h) | Zero-shot vs. few-shot vs. CoT on the same task (e.g. classify support tickets). Record accuracy on 20 examples |
| 3 (2h) | Structured output: make the model return JSON and validate it with Pydantic (week 2 skill) |
| Weekend (4h) | Build the lab below. Install Flowise (or use a hosted version) and rebuild one prompt visually |

## Deliverable: Modular Prompt Assembly Lab
`projects/week03/prompt_lab/`:
- A prompt built from separate modules: **role, task, rules, examples, output format, user input**
- A messy "erratic" starting agent (you write a vague prompt that behaves badly)
- Fix it one module at a time, with a table showing before/after results on 20 test inputs
- Rebuild the final prompt as a Flowise flow (screenshot it)

## Check yourself
- Why does the same prompt give different answers?
- Give one case each where you'd use prompting, RAG and fine-tuning.
- What is context engineering, and why isn't it just "writing a good prompt"?
- How would you explain "probabilistic software" to your engineering lead?

## Stretch
Try two different models on the same 20 inputs and compare quality, speed and cost.
