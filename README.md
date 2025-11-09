# rag-document-chunking-pgvector

# 🧩 Document Chunking and Indexing with pgvector

A Jupyter Notebook demonstrating how to split long documents into semantically coherent chunks, embed them using OpenAI’s models, and index them in PostgreSQL with pgvector for retrieval-augmented generation (RAG) systems.

---

## 🚀 Overview

This notebook walks through:
- **Chunking** large text into overlapping segments using LangChain’s `RecursiveCharacterTextSplitter`
- **Embedding** each chunk using OpenAI’s `text-embedding-3-small` model
- **Indexing** the results in PostgreSQL with the `pgvector` extension
- **Storing metadata** (title, source, timestamp) for semantic retrieval

Chunking may sound simple, but it’s the foundation of accurate, context-aware AI systems.

---

## ⚙️ Setup

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/rag-document-chunking-pgvector.git
cd rag-document-chunking-pgvector
```

### 2. Create and activate a virtual environment
```bash
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate
```
### 3. Install dependencies
```bash
#pip install langchain langchain-openai openai psycopg2-binary pgvector psycopg2 tiktoken langchain_text_splitters 
```
### 4. Enable pgvector in your postgres database
```bash
CREATE DATABASE vectordb;
\c vectordb
CREATE EXTENSION IF NOT EXISTS vector;
```
