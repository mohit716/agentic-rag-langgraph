# Agentic RAG with LangGraph

This project demonstrates how to build a **custom agentic Retrieval-Augmented Generation (RAG) system** using **LangGraph** and **LangChain**.  
It combines retrieval, grading, and rewriting logic to let an LLM decide *when* to fetch external context and *when* to answer directly — a hybrid RAG architecture.

---

## Overview

By the end of this notebook, you’ll have a working RAG agent that can:

1. **Fetch and preprocess** documents (web pages, PDFs, or text)
2. **Index** them into a vectorstore for semantic search
3. **Build a retriever tool** the agent can invoke when needed
4. **Decide** whether to call the retriever or respond directly
5. **Grade document relevance** and rewrite the query if needed
6. **Generate a final answer** based on retrieved context

This implementation uses LangGraph’s **state-based graph API** to chain the following nodes:
