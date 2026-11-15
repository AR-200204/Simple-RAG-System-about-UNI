# Uni RAG System

A small Python project exploring how Retrieval-Augmented Generation (RAG) works, from loading documents to generating answers with a local language model.

The idea is simple: instead of asking an LLM to answer everything from its training data, give it relevant information from your own documents and let it answer using that context.

## What I'm Working On

- Loading documents from Markdown files.
- Splitting large documents into smaller chunks.
- Generating text embeddings using Ollama.
- Finding relevant information through semantic similarity.
- Using a local LLM to generate answers based on retrieved content.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Ollama | Running models locally |
| Nomic Embed Text | Generating embeddings |
| Qwen3 4B | Generating responses |
| NumPy | Working with embedding vectors |
| uv | Python project and dependency management |

## Models

This project currently uses two Ollama models:

- `nomic-embed-text` – Converts text into numerical vectors.
- `qwen3:4b-instruct` – Generates answers from the provided context.

Download them using:

```bash
ollama pull nomic-embed-text
ollama pull qwen3:4b-instruct
```

Make sure Ollama is running before executing the application.

## Project Structure

```text
rag/
│
├── handbook.md
├── chunking.py
├── main.py
├── pyproject.toml
├── uv.lock
└── README.md
```

*The structure may change as the project develops.*

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Simple-RAG-System.git
cd Simple-RAG-System
```

### 2. Create a virtual environment

```bash
uv venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
uv sync
```

If dependencies have not yet been added to `pyproject.toml`, install them with:

```bash
uv add requests numpy
```

### 4. Run the project

```bash
python main.py
```

## Understanding the RAG Pipeline

The basic workflow looks like this:

```text
        Document
            |
            v
      Text Extraction
            |
            v
         Chunking
            |
            v
       Embeddings
            |
            v
      Vector Storage
            |
            v
     Similarity Search
            |
            v
    Relevant Context
            |
            v
       Local LLM
            |
            v
          Answer
```

## Why This Project?

I'm building this project to understand the components behind RAG systems rather than relying entirely on ready-made frameworks.

The goal is to experiment with each stage, understand how the components work together, and gradually build a working document-based question-answering system.

## Current Status

Work in progress. I'm developing the pipeline step by step, starting with document loading, text chunking, and embeddings.

More features will be added as the project develops.

---

**Author:** YOUR_NAME


