# Week 7: Advanced RAG and Agent Memory

**Syllabus:** Module 5 (part 2) | **Phase:** Memory and knowledge | **Project:** Memory-Enabled Support System

## Why this matters (PM lens)
A support bot that forgets you between chats feels broken. Memory is a product feature with privacy, cost and trust implications: what do we remember, for how long, and who can see it?

## Concepts in plain English
- **Query rewriting:** the user's question is often vague ("what about for Pune?"). Have the LLM rewrite it into a standalone search query before retrieving.
- **Hybrid search:** keyword search (exact terms, product codes) plus semantic search (meaning), merged. Catches what either alone misses.
- **Re-ranking:** retrieve 20, then pick the best 5.
- **Short-term memory:** the current conversation (a rolling window, or summarized when too long).
- **Long-term memory:** facts about a user stored in a database across sessions (name, plan, past issues, preferences).
- **Memory design questions:** What to store? When to update or forget? How to avoid storing wrong or sensitive things?

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Add query rewriting to your week 6 bot. Re-run your 25 questions and compare |
| 2 (2h) | Add hybrid search (keyword + vector) and measure the difference |
| 3 (2h) | Build short-term memory: conversation history with summarization after N turns |
| Weekend (4h) | Long-term profile in SQLite. Build the deliverable |

## Deliverable: Memory-Enabled Support System
`projects/week07/support_bot/`:
- Dual-layer memory: short-term chat state **and** a permanent per-user profile database
- RAG over a support knowledge base (reuse week 6)
- Demo script: User A chats, leaves, returns the next day and the bot remembers their plan and open issue
- User B must **not** see User A's data (test it!)
- A command to view and delete a user's stored data
- Updated results table: v1 vs. v2 retrieval quality

## Check yourself
- What's the difference between short-term and long-term memory in an agent?
- When does hybrid search beat pure semantic search?
- What would you refuse to store about a user, and why?
- How would a user ask the bot to forget them?

## Stretch
Let the agent decide for itself when something is worth saving to long-term memory.
