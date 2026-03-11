# AI Voice Chatbot with ElevenLabs + OpenAI + RAG

An AI Voice Assistant that answers user questions using OpenAI, retrieves information from a Vector Database (Qdrant), and responds with natural voice using ElevenLabs.

The system uses n8n as the orchestration engine and supports document-based question answering through Retrieval-Augmented Generation (RAG).

---

# Project Overview

This project demonstrates how to build a voice AI agent capable of:

- Receiving voice questions from users
- Converting them to text
- Retrieving relevant information from a vector database
- Generating a response using an LLM
- Returning the answer as natural speech

The architecture combines voice AI, vector search, and LLM reasoning.

---

# Workflow Preview

<img width="290" height="521" alt="Screenshot 2026-03-09 200802" src="https://github.com/user-attachments/assets/e6b943ed-a27a-48e9-a0cf-889c7c3c1f8a" />

---

# Architecture

The system consists of several stages.

## 1 Voice Agent (ElevenLabs)

A conversational agent is created in ElevenLabs which:

- Greets the user
- Receives voice input
- Sends the question to n8n through a webhook

The agent can be embedded directly into websites using the ElevenLabs widget.

---

## 2 Vector Database (Qdrant)

The system creates a Qdrant collection that stores document embeddings.

Documents are processed and converted into vectors that enable semantic search.

---

## 3 Document Vectorization

Documents stored in Google Drive are:

1. Downloaded automatically  
2. Split into chunks  
3. Converted into embeddings  
4. Stored inside the Qdrant vector database  

This allows the AI to answer questions based on document content.

---

## 4 RAG Question Answering

When the user asks a question:

1. ElevenLabs sends the question to n8n webhook  
2. The AI Agent retrieves relevant documents from Qdrant  
3. The OpenAI model generates an answer  
4. The response is returned to ElevenLabs  
5. ElevenLabs converts the answer to speech  

---

# Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenAI | LLM reasoning |
| ElevenLabs | Voice synthesis |
| Qdrant | Vector database |
| Google Drive | Document storage |
| LangChain Nodes | AI orchestration |

---

# Key Features

- Voice AI interaction
- Retrieval-Augmented Generation (RAG)
- Document-based question answering
- Vector search using Qdrant
- Natural speech responses
- Website widget integration

---

  

---

# Setup

To run the workflow you need:

- ElevenLabs account
- OpenAI API key
- Qdrant vector database
- n8n instance
- Google Drive connection

---

# Example Use Cases

This system can be used for:

- Restaurant voice assistants
- Customer support AI
- AI receptionists
- Business FAQ bots
- Knowledge base assistants

---

# Future Improvements

Possible improvements include:

- Speech-to-text optimization
- Multi-language support
- CRM integrations
- Website analytics
- AI call agents

---

# Author

Mohammad Alkhatib
