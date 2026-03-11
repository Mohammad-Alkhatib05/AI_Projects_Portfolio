# Build a Document QA System with RAG

A smart **Document Question Answering system** built with **n8n**, **Milvus**, **Cohere Embeddings**, **OpenAI GPT-4o**, and **Google Drive**.

This workflow automatically watches a Google Drive folder for new PDF files, extracts their content, splits the text into chunks, generates embeddings, stores them in **Milvus**, and lets users ask questions through a **RAG agent**. :contentReference[oaicite:1]{index=1}

---

## Overview

This project demonstrates a practical **Retrieval-Augmented Generation (RAG)** pipeline for document-based Q&A.

### What it does
- Watches a specific **Google Drive** folder for newly added PDF files
- Downloads each new file automatically
- Extracts text from the PDF
- Splits the document into chunks
- Generates multilingual embeddings using **Cohere**
- Inserts the embeddings into **Milvus**
- Uses an **OpenAI GPT-4o** powered agent to answer user questions based on retrieved chunks from the vector database :contentReference[oaicite:2]{index=2}

---

## Workflow Architecture

### Ingestion Flow
`Google Drive Trigger → Download File → Extract PDF Text → Split Text → Create Embeddings → Insert into Milvus`

### Chat Flow
`Chat Trigger → RAG Agent → Retrieve Relevant Chunks from Milvus → Answer with GPT-4o` :contentReference[oaicite:3]{index=3}

---

## Project Preview

<img width="1015" height="535" alt="Screenshot 2026-03-09 212858" src="https://github.com/user-attachments/assets/3546d528-ef82-4e64-855a-c7a70f87d6bd" />
<img width="1015" height="535" alt="Screenshot 2026-03-09 212858" src="https://github.com/user-attachments/assets/3546d528-ef82-4e64-855a-c7a70f87d6bd" />

---

## Tech Stack

- **n8n** for orchestration
- **Google Drive** for document input
- **Milvus** for vector storage and retrieval
- **Cohere Embeddings** (`embed-multilingual-v3.0`) for vectorization
- **OpenAI GPT-4o** for answer generation
- **PDF Extractor** for document parsing
- **Buffer Memory** for conversational context handling :contentReference[oaicite:4]{index=4}

---

## Key Features

- Automated document ingestion from Google Drive
- PDF text extraction
- Recursive text chunking
- Multilingual embeddings with Cohere
- Fast semantic search with Milvus
- Conversational RAG agent
- Clean modular workflow in n8n :contentReference[oaicite:5]{index=5}

---

## Chunking Strategy

This workflow uses a recursive character text splitter with:

- **Chunk Size:** 700
- **Chunk Overlap:** 60

This helps preserve context while improving retrieval quality. :contentReference[oaicite:6]{index=6}

---

## How It Works

### 1) File Monitoring
A Google Drive trigger watches a specific folder for new files.

### 2) File Download
Whenever a new file is added, the workflow downloads it automatically.

### 3) Text Extraction
The PDF content is extracted using the file extraction node.

### 4) Document Chunking
The extracted text is split into smaller chunks for better embedding and retrieval.

### 5) Embedding Generation
Each chunk is converted into vector embeddings using **Cohere**.

### 6) Vector Storage
The chunks and embeddings are inserted into a **Milvus** collection.

### 7) User Question Answering
When a user sends a message, the RAG agent retrieves relevant chunks from Milvus and uses **GPT-4o** to generate an answer. :contentReference[oaicite:7]{index=7}

---

## Author

Mohammad Alkhatib
