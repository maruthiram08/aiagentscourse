# Week 5: Reasoning Loops, Planning and State

**Syllabus:** Module 3 | **Phase:** Making agents act | **Project:** Autonomous Planning Workflow

## Why this matters (PM lens)
This is the heart of "agentic". Here you decide how much freedom the agent gets: a fixed script, a plan it follows, or a loop where it figures things out. Each choice trades **flexibility against predictability and cost**, and that's a product decision.

## Concepts in plain English
- **ReAct:** Think, Act (use a tool), Observe the result, repeat until done. Flexible, but can wander.
- **Plan-and-Execute:** make a full plan first, then run the steps. More predictable and easier to review, but weaker when surprises happen.
- **Reflection / self-correction:** the agent critiques its draft and fixes it. Better quality, higher cost.
- **Goal decomposition:** breaking "research competitors" into sub-tasks.
- **Dynamic routing:** choosing the next step based on what just happened.
- **State:** the agent's working memory: goal, plan, completed steps, results, errors.
- **State machine:** explicit stages (PLANNING, EXECUTING, REVIEWING, DONE, FAILED) with rules for moving between them. This is how you make agents controllable.
- **Error recovery:** retry, replan, escalate to a human, or stop safely. Always set a **maximum number of steps**.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Build a bare ReAct loop by hand (a `while` loop calling your week 4 tools). Log every thought/action/observation |
| 2 (2h) | Add a hard step limit and a "give up gracefully" path. Trigger infinite loops on purpose |
| 3 (2h) | Build a Plan-and-Execute version of the same task. Compare with ReAct on 5 tasks (success, steps, cost) |
| Weekend (4h) | Add a reflection step and an explicit state machine. Build the deliverable |

## Deliverable: Autonomous Planning Workflow
`projects/week05/planner/`:
- Takes a goal such as *"Plan a 3-day offsite for 20 people under a budget"* or *"Summarize 5 competitor pricing pages"*
- Decomposes it into sub-tasks, executes with tools, reflects and corrects
- Explicit states with a state diagram (draw it)
- Error recovery: at least 2 failure scenarios shown (tool failure, bad plan)
- A 1-page comparison: ReAct vs. Plan-and-Execute on your tasks

## Check yourself
- When would you choose Plan-and-Execute over ReAct for a product?
- What stops an agent from looping forever and burning money?
- What belongs in agent "state"?
- What would you let the agent decide alone, and what needs a human?

## Stretch
Add a "human checkpoint" state where the agent pauses for approval before step 3.
