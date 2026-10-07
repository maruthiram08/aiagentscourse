# Week 8: LangChain, LangGraph and Visual Tools

**Syllabus:** Module 6 (part 1) | **Phase:** Frameworks and teams | **Project:** No-Code Visual Graph Prototype

## Why this matters (PM lens)
Your team will likely use a framework rather than raw code. You need to know what frameworks give you (speed, structure), what they cost (complexity, lock-in), and when a visual tool is enough for a prototype. **This is also the week you pick your capstone.**

## Concepts in plain English
- **LangChain:** building blocks (models, prompts, retrievers, tools) you chain together.
- **LangGraph:** you model the agent as a **graph**: nodes (steps), edges (what comes next), **conditional edges** (branching) and **cycles** (loops). It's your week 5 state machine, as a library.
- **Persistent state and checkpoints:** pause, resume, and human-in-the-loop.
- **Flowise / LangFlow:** build the same flows by dragging boxes. Great for prototypes and demos to stakeholders. Limited for complex logic.
- **Framework trade-offs:** when raw code beats a framework, and the reverse.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | LangChain basics: prompt, model, output parser, and a simple chain |
| 2 (2h) | LangGraph: rebuild your week 5 planner as a graph with a conditional edge and a loop |
| 3 (2h) | Flowise: build a RAG chatbot on your documents visually |
| Weekend (4h) | LangFlow (or a second Flowise flow) for an agent with tools. **Choose your capstone** and write its 1-page proposal (see `CAPSTONE.md`) |

## Deliverable: No-Code Visual Graph Prototype
`projects/week08/`:
- A Flowise or LangFlow flow with a retriever, an LLM and at least one tool, with exported JSON and screenshots
- Your week 5 planner rebuilt in LangGraph, with a drawn graph
- A short comparison: *raw code vs. LangGraph vs. visual tool* on effort, control, debuggability
- Capstone proposal (1 page), approved by you against the rubric

## Check yourself
- What does a conditional edge do, and where did you use one?
- When would you ship a Flowise flow to production, and when would you not?
- What's the downside of heavy framework use?
- Can you draw your capstone as a graph on a whiteboard?

## Stretch
Add a human-approval node using LangGraph checkpoints.
