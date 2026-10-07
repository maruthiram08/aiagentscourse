# Week 9: CrewAI, AutoGen and Multi-Agent Collaboration

**Syllabus:** Module 6 (part 2) + Module 7 | **Phase:** Frameworks and teams | **Project:** Multi-Agent Orchestrated "Crew"

## Why this matters (PM lens)
"Let's use multiple agents" is an easy thing to say and an expensive thing to do. More agents means more cost, latency and ways to fail. A good PM knows when one agent is enough. Be skeptical, and learn the patterns so you can judge.

## Concepts in plain English
- **CrewAI:** define agents by **role, goal and backstory**, give them tasks, run as a crew. Simple, readable.
- **AutoGen:** agents that talk to each other in conversation, event-driven. More flexible, more to manage.
- **Orchestration topologies:**
  - *Sequential:* A, then B, then C (a pipeline)
  - *Hierarchical:* a supervisor delegates to workers and checks results
  - *Decentralized network:* peers talk freely (powerful and hard to control)
- **Inter-agent communication:** direct messages, broadcasts, and passing **structured data** (use Pydantic models, not loose text).
- **Conflict resolution:** two agents disagree, or edit the same shared document. Solutions: a single owner per resource, locks, a judge agent, a voting rule.
- **Race conditions:** agents changing shared state at the same time giving unpredictable results.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | CrewAI: a sequential crew of 3 (researcher, analyst, writer) |
| 2 (2h) | Switch to a hierarchical supervisor/worker setup. Compare output and cost |
| 3 (2h) | AutoGen: a two-agent conversation (writer and critic) with a termination rule |
| Weekend (4h) | Shared state and conflict handling. Build the deliverable. Compare with a **single agent** doing the same task |

## Deliverable: Multi-Agent "Crew"
`projects/week09/crew/`:
- 3 or more specialized agents solving one shared data-processing task (e.g. read a CSV of customer feedback, categorize, find themes, write an executive summary)
- Typed messages between agents
- A deliberately induced conflict (two agents disagree or write the same thing) and your resolution mechanism
- **Single-agent baseline** vs. crew: quality, cost, time. Write your verdict honestly
- A diagram of your topology and why you chose it

## Check yourself
- When is one agent better than a crew?
- Compare supervisor/worker with a decentralized network on control vs. flexibility.
- What is a race condition between agents, and how do you prevent it?
- Why pass structured data, not free text, between agents?

## Stretch
Run the AutoGen version of the same task and compare with CrewAI on setup effort and control.
