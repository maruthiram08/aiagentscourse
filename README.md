# Agentic AI in 12 Weeks: A Course for Product Managers

A 3-month, self-paced plan based on the *Professional Certificate in Agentic AI and Applications* syllabus (8 modules, ~8 hands-on projects, 1 capstone). It assumes **no prior coding experience**.

## The goal

By week 12 you will have:
- Built and shipped a working multi-agent system in a Docker container
- Written about 10 small agent projects you can show people
- Enough technical depth to make real product decisions: what an agent can and can't do, what it costs, how to test it, and how it fails

You are not training to be a full-time engineer. You are training to be a PM who can **build prototypes, judge feasibility, and talk to engineers as a peer**.

## Assumptions (change the plan if these are wrong)

| Assumption | Detail |
|---|---|
| Time | About 10 hours a week: 3 weekday sessions of ~2 hours, plus one ~4-hour weekend block |
| Coding help | You will use an AI coding assistant (Claude Code or similar) to write and explain code. This is the learning method, not cheating. See "How to learn" below |
| Budget | About $30-60 in LLM API credits across the whole course. Set a hard spending limit on your account in week 1 |
| Start date | Any Monday. Week numbers are relative |

## The 12-week map

| Phase | Week | Topic | Syllabus module | Project you build |
|---|---|---|---|---|
| **1. Foundations** | 1 | Setup + Python from zero | M1 | Small command-line tools |
| | 2 | Python for AI: types, async, APIs, retries | M1 | Resilient API-calling script |
| | 3 | How LLMs work, prompting, context engineering | M2 | **Modular Prompt Assembly Lab** |
| **2. Making agents act** | 4 | Tools, function calling, MCP | M4 | **Function-Calling Assistant** |
| | 5 | Reasoning loops, planning, state | M3 | **Autonomous Planning Workflow** |
| **3. Memory and knowledge** | 6 | Embeddings, vector DBs, RAG | M5 | **RAG Document Q&A Bot** |
| | 7 | Advanced RAG + agent memory | M5 | **Memory-Enabled Support System** |
| **4. Frameworks and teams** | 8 | LangChain, LangGraph + visual tools | M6 | **No-Code Visual Graph Prototype** |
| | 9 | CrewAI, AutoGen, multi-agent patterns | M6, M7 | **Multi-Agent "Crew"** |
| **5. Production** | 10 | Evaluation and observability | M8 | **Production Observability Pipeline** |
| | 11 | Security, guardrails, Docker, CI/CD | M8 | Hardened, containerized agent |
| **6. Capstone** | 12 | Design, build, test, ship | All | **Capstone project** (see `CAPSTONE.md`) |

### Two deliberate changes from the syllabus order

1. **Tools (Module 4) comes before reasoning loops (Module 3).** An agent's "reasoning and acting" loop only makes sense once you've seen it call a tool.
2. **A no-code tool (Flowise) is introduced early, in week 3, not just in week 8.** Seeing an agent as boxes and arrows first makes the code easier to read later.

### What gets less time

- **Pandas/Polars:** a light touch in week 2 only. You need to read a table, not master data science.
- **Fine-tuning and RLHF:** concept-level only (week 3). You need to know *when* to fine-tune vs. prompt vs. use RAG, not how to train a model.

## How each week is structured

Every file in `weeks/` follows the same shape:

1. **Why this matters** (the PM lens)
2. **Concepts in plain English**
3. **Schedule** (Session 1, 2, 3, weekend build)
4. **Deliverable** (what to have by Sunday)
5. **Check yourself** (questions you should be able to answer)
6. **Stretch** (optional)

## How to learn (the method)

1. **Run it before you understand it.** Get the example working, then ask your AI assistant to explain every line.
2. **Break it on purpose.** Change an input, remove a line, send bad data. See what fails. Agents are about failure handling.
3. **Keep a build log.** After each session write 3 lines: what I built, what broke, what I learned. This becomes your portfolio story.
4. **Explain it back.** Every Friday, explain the week's topic in plain English in 5 sentences, as if to a stakeholder. If you can't, you haven't got it yet.
5. **Ask the assistant to teach, not just do.** Useful prompt: *"I'm a PM with no coding background. Explain this code line by line, then give me a 3-question quiz."*

## Checkpoints

| End of week | You should be able to... |
|---|---|
| 3 | Write a short Python script, call an LLM, and explain why the same prompt gives different answers |
| 5 | Show an agent that decides on its own which tool to use and recovers from an error |
| 7 | Show a bot that answers from your own documents and remembers a returning user |
| 9 | Show 3 agents collaborating on one task, and explain which pattern you chose and why |
| 11 | Show your agent resisting a prompt-injection attempt and running in Docker |
| 12 | Demo the capstone end to end and present its quality metrics and cost per task |

## Repo contents

- `weeks/week-01.md` to `weeks/week-12.md`: the weekly lessons
- `CAPSTONE.md`: capstone brief, ideas and grading rubric
- `GLOSSARY.md`: plain-English definitions of every term
- `BUILD_LOG.md`: your running journal (fill it in as you go)
- `projects/`: where your code goes, one folder per project

## If you fall behind

Don't skip weeks 4, 5, 6 or 10. They are the core. If you must cut, cut in this order: Pandas/Polars (week 2), LangFlow (week 8), AutoGen (week 9), the stretch goals everywhere.
