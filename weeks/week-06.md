# Week 6: Embeddings, Vector Databases and RAG

**Syllabus:** Module 5 (part 1) | **Phase:** Memory and knowledge | **Project:** RAG-Powered Document Q&A Bot

## Why this matters (PM lens)
Most enterprise value in agents comes from letting them answer from **your** data (policies, contracts, tickets, wikis). RAG is the most common pattern you'll be asked to scope. Knowing why it fails (bad chunks, wrong retrieval) will make you a much better PM on these projects.

## Concepts in plain English
- **Embeddings:** text turned into numbers so that similar meanings sit close together.
- **Vector database:** stores embeddings and quickly finds the nearest ones. Start with **ChromaDB** (easiest), try **FAISS** (fast, in-memory), and read about **Pinecone** (hosted service).
- **RAG flow:** question, embed it, retrieve top matches, put them in the prompt, LLM answers **citing sources**.
- **Document parsing:** getting clean text out of PDFs, Word and web pages (this step is where many projects quietly fail).
- **Chunking:** splitting documents. Too big and the answer gets diluted. Too small and context is lost. Try fixed-size, overlap, and **semantic** chunking.
- **Metadata filtering:** only search documents from a given year, department or product.

## Schedule
| Session | Do |
|---|---|
| 1 (2h) | Create embeddings for 20 sentences. Find the nearest to a query. See that "refund" matches "money back" |
| 2 (2h) | Load documents into ChromaDB. Query it. Add metadata and filter |
| 3 (2h) | Parse a real PDF. Compare 3 chunking strategies on the same questions |
| Weekend (4h) | Wire retrieval into an LLM answer with citations. Build the deliverable |

## Deliverable: RAG Document Q&A Bot (v1)
`projects/week06/rag_bot/`:
- Corpus: 10 or more real documents (company handbook, public policy PDFs, product manuals)
- Chunking with overlap, metadata (source, section, date)
- Answers with citations; says "I don't know" when the documents don't cover it
- A **test set of 25 questions** (including 5 unanswerable ones) with a hand-scored results table
- Vector store runs in ChromaDB; FAISS comparison noted

## Check yourself
- Why can't you just paste all documents into the prompt?
- Name three reasons RAG gives a bad answer (hint: parsing, chunking, retrieval).
- What's an embedding, in one sentence for a non-technical stakeholder?
- How do you make the bot refuse when it doesn't know?

## Stretch
Add a simple web UI (Streamlit) so a non-technical colleague can try it.
