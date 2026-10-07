# Week 1: Setup and Python from Zero

**Syllabus:** Module 1 (Clean code, OOP basics) | **Phase:** Foundations

## Why this matters (PM lens)
Every agent is a Python program. You won't write it all by hand, but you must be able to read it, run it, and spot what's wrong. This week removes the fear.

## Concepts in plain English
- **Python basics:** variables, lists, dictionaries, `if`, loops, functions. A dictionary is a labelled box of values, and it's how almost all agent data looks.
- **Modules and packages:** reusing code others wrote (`pip install`).
- **Virtual environment:** a clean, separate toolbox per project so projects don't clash.
- **Classes (OOP):** a blueprint that bundles data and behavior, e.g. a `Customer` with a `name` and a `send_email()` action.
- **Composition:** building big things by plugging small objects together (an `Agent` *has* a `Tool`), rather than one giant tangle.
- **Git:** saving snapshots of your work.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Install Python 3.11+, VS Code (or use the cloud environment), Git. Create a virtual environment. Run "hello world". Set up an LLM API account and a **spending cap** |
| 2 (2h) | Variables, strings, lists, dictionaries, loops, functions. Use an AI assistant to explain each snippet |
| 3 (2h) | Reading and writing files (CSV/JSON). Handling errors with `try/except` |
| Weekend (4h) | Classes and composition. Build the deliverable below |

## Deliverable
Three tiny command-line tools in `projects/week01/`:
1. **Expense summarizer:** reads a CSV of expenses, prints total per category
2. **Meeting-notes cleaner:** reads a text file, prints action items (lines starting with "TODO")
3. **Tiny agent skeleton:** classes `Agent` and `Tool`, where an agent holds a list of tools and can "use" one by name (no AI yet)

Commit all three to Git and update `BUILD_LOG.md`.

## Check yourself
- What's the difference between a list and a dictionary?
- Why do we use a virtual environment?
- What does "composition" mean, and why prefer it for agents?
- What happens if a file you try to read doesn't exist, and how do you handle it?

## Stretch
Add a second tool to your skeleton and make the agent pick one using a simple `if` rule.
