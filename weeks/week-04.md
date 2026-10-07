# Week 4: Tools, Function Calling and MCP

**Syllabus:** Module 4 | **Phase:** Making agents act | **Project:** Function-Calling Assistant

## Why this matters (PM lens)
Tools are what turn a chatbot into an agent. Every "can the agent do X?" product question becomes "do we have a tool for X, and is it safe?". Tool design is product design.

## Concepts in plain English
- **Function calling:** you describe each tool with a JSON schema (name, purpose, inputs). The model replies "call this tool with these inputs". **Your code** runs it and sends the result back.
- **Good tool descriptions:** the model chooses tools by reading your description. Vague descriptions give wrong choices.
- **External systems:** web APIs, databases (basic SQL: `SELECT`, `WHERE`, `JOIN`), and **sandboxes** (a safe place to run code the agent writes).
- **Tool safety:** read-only vs. write tools, confirmation before risky actions, limiting what each tool can touch.
- **MCP (Model Context Protocol):** a standard connector so one tool server works with many agents/apps. Think of it as USB-C for agent tools.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Define one tool (e.g. `get_weather`) with a JSON schema. Watch the model request it and return the result |
| 2 (2h) | Add 3 more tools. Test ambiguous requests and observe wrong choices; fix by rewriting descriptions |
| 3 (2h) | SQL basics. Create a small SQLite database and a `query_orders` tool (read-only) |
| Weekend (4h) | Code-execution sandbox tool. Connect to an existing MCP server and use its tools. Build the deliverable |

## Deliverable: Function-Calling Assistant
`projects/week04/assistant/`:
- 4 or more tools: a web API, a SQLite database query, a calculator/sandbox, and one of your choice
- Pydantic validation on every tool input
- Handles tool errors gracefully (the model sees the error and recovers)
- A test sheet of 15 requests with the expected tool and the actual tool chosen
- One tool exposed or consumed via MCP

## Check yourself
- Who actually executes a function call: the model or your code?
- Why might a model pick the wrong tool, and how do you fix it?
- Which of your tools would you never give "write" access to, and why?
- What problem does MCP solve compared to custom integrations?

## Stretch
Add a human-approval step before any tool that changes data.
