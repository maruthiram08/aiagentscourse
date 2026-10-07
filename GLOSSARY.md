# Glossary (plain English)

| Term | Meaning |
|---|---|
| **Agent** | An LLM that doesn't just answer. It decides what to do next, uses tools, and loops until a goal is met |
| **LLM** | Large Language Model. Predicts the next piece of text based on the text so far |
| **Token** | A chunk of text (about 3/4 of a word). You pay and are limited by tokens |
| **Context window** | How much text the model can "see" at once. Everything outside it is forgotten |
| **Prompt** | The instructions and data you send to the model |
| **Context engineering** | Deciding exactly what goes into the context window each time (instructions, examples, documents, memory) |
| **Zero-shot / few-shot** | Asking with no examples vs. with a few examples |
| **Chain-of-Thought (CoT)** | Getting the model to reason step by step before answering |
| **Fine-tuning** | Further training a model on your examples to change its behavior |
| **RLHF** | Reinforcement Learning from Human Feedback. Humans rank outputs and the model learns to prefer the good ones |
| **Hallucination** | A confident answer that is made up |
| **Tool / function calling** | The model outputs a structured request ("call `get_weather` with city=Pune") and your code runs it |
| **JSON schema** | A strict description of the shape of data (field names and types) |
| **MCP** | Model Context Protocol. A standard "plug" so any agent can connect to any tool or data source |
| **ReAct** | Reason, then Act, then observe the result, then repeat |
| **Plan-and-Execute** | Make a full plan first, then carry out the steps |
| **Reflection** | The agent critiques its own output and retries |
| **State** | Everything the agent knows right now (messages, goal, progress) |
| **State machine** | A set of defined stages with rules for moving between them |
| **Embedding** | A list of numbers that captures the meaning of a text. Similar meanings give nearby numbers |
| **Vector database** | A database that finds the items nearest in meaning (FAISS, ChromaDB, Pinecone) |
| **RAG** | Retrieval-Augmented Generation. Look up relevant documents first, then have the LLM answer using them |
| **Chunking** | Splitting documents into pieces before embedding |
| **Hybrid search** | Combining keyword search with meaning-based search |
| **Short-term / long-term memory** | This conversation vs. things remembered across sessions |
| **LangChain / LangGraph** | Libraries for building LLM apps; LangGraph models agents as a graph of steps with loops |
| **CrewAI / AutoGen** | Frameworks for teams of agents with roles |
| **Flowise / LangFlow** | Drag-and-drop tools to build agent flows without code |
| **Supervisor/worker** | One manager agent delegates to specialist agents |
| **Race condition** | Two agents changing the same thing at once with unpredictable results |
| **Eval** | A repeatable test that scores agent quality |
| **Faithfulness** | Does the answer stick to the retrieved sources? |
| **Ragas / TruLens** | Tools that score faithfulness, relevance and grounding |
| **Observability / trace** | Seeing every step an agent took, with timing and cost (LangSmith, AgentOps) |
| **Prompt injection** | Malicious text that tricks the agent into ignoring its instructions |
| **Guardrails** | Rules that check inputs and outputs (e.g. NeMo Guardrails) |
| **Docker / container** | A sealed box holding your app and everything it needs, so it runs the same anywhere |
| **CI/CD** | Automatic testing and deployment every time you change the code |
| **Async** | Doing other work while waiting for a slow call (like an API) |
| **Pydantic** | A Python library that rejects data in the wrong shape |
| **API** | A way for programs to talk to each other over the internet |
| **Rate limit / retry / backoff** | Providers limit request speed; you retry after waiting longer each time |
