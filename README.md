# 🧠 LangGraph PDF Chatbot with Streamlit

A **multi-utility AI chatbot** built using **LangGraph**, **LangChain**, and **Streamlit** that supports document-based question answering, web search, calculator tools, and persistent multi-threaded conversations.

This project demonstrates a **real-world agentic AI system** with Retrieval-Augmented Generation (RAG), intelligent tool calling, and long-term memory checkpointing.

---

## 🚀 Features

- 📄 **Chat with PDFs (RAG)**
  - Upload PDFs and ask contextual questions
  - Automatic text chunking, embedding, and FAISS indexing

- 🧠 **Agentic Tool Usage**
  - DuckDuckGo Web Search
  - Calculator for arithmetic operations
  - Smart tool selection using LangGraph

- 🧵 **Multi-Thread Conversations**
  - Each conversation has a unique `thread_id`
  - Switch between past conversations
  - Thread-specific document memory

- 💾 **Persistent Memory**
  - SQLite-based checkpointing
  - Conversations persist across app restarts

- ⚡ **Live Tool Status**
  - Real-time tool execution feedback in Streamlit UI

---

## 🏗️ Architecture Overview

![LangGraph PDF Chatbot Architecture](assets/architecture.png)

> High-level system architecture illustrating LangGraph agent flow, tool routing, and the RAG pipeline.

### Architecture Flow

1. User interacts with the chatbot via **Streamlit UI**
2. Requests are routed to a **LangGraph State Graph**
3. The **LLM (ChatGroq)** decides whether to:
   - Respond directly
   - Invoke a tool
4. Available tools:
   - DuckDuckGo Search
   - Calculator
   - RAG Pipeline (PDF → Chunking → Embedding → FAISS → Retriever)
5. Retrieved context is injected into the LLM
6. Final response is streamed back to the UI
7. Conversation state is checkpointed in **SQLite**

---

## 🛠️ Tech Stack

- **LLM:** ChatGroq
- **Agent Framework:** LangGraph
- **RAG Pipeline:** LangChain + FAISS
- **Embeddings:** HuggingFace MiniLM
- **UI:** Streamlit
- **Database:** SQLite
- **Search Engine:** DuckDuckGo
- **Language:** Python

---
