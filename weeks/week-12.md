# Week 12: Capstone Week

**Syllabus:** Intelligent Capstone Project | **Phase:** Capstone

You chose and scoped your capstone in week 8. This week you build, harden, measure and ship it. See `CAPSTONE.md` for the brief and rubric.

## Day-by-day plan (about 10-14 hours; take extra days if you can)

| Day | Focus | Done when |
|---|---|---|
| Mon | **Blueprint:** finalize sub-tasks, agent roles, tools, data, state diagram | One-page architecture diagram committed |
| Tue | **Engine, part 1:** core workflow runs end to end on one happy-path input | Demo of the happy path |
| Wed | **Engine, part 2:** planning loop, state machine, error recovery, step and cost limits | 3 failure scenarios handled |
| Thu | **Guardrails:** eval set (30+ cases), Ragas/TruLens scores, prompt injection tests, tracing on | Metrics table and red-team table |
| Fri | **Ship:** Dockerfile, README, CI workflow, run from a clean machine/container | `docker run` works for someone else |
| Sat | **Polish and present:** record a 5-minute demo; write the product brief | Demo video and brief done |
| Sun | **Retro:** update `BUILD_LOG.md`, write what you'd do next | Portfolio-ready repo |

## Final deliverables
1. Working agentic system in `projects/capstone/`
2. Docker container that runs it
3. Architecture diagram
4. Eval report (metrics before/after, cost per task, latency)
5. Security report (attacks tried and defenses)
6. 5-minute demo video
7. **PM brief (2 pages):** the problem, why agents, the design choices and their trade-offs, risks, and what you'd need to take it to real users

## Check yourself
- Can someone who didn't build it run it from your README in 10 minutes?
- Can you say what it costs per task and whether the business case works?
- What is the first thing that will go wrong in the real world, and what did you do about it?

## After the course
Pick a real problem at your workplace and prototype it. Teach a colleague what you learned (the best test of understanding), and keep adding to your build log.
