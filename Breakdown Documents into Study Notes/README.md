# Breakdown Documents into Study Notes

An AI-powered document processing workflow that automatically converts documents into structured study materials using Retrieval-Augmented Generation (RAG).

This workflow watches a folder for new documents, processes them using AI models, and generates structured study notes such as study guides, timelines, and briefing documents.

---

# Project Overview

This automation transforms raw documents into organized study material automatically.

The system:

• Detects new files in a folder  
• Extracts text from PDF, DOCX, or TXT files  
• Stores document knowledge in a vector database  
• Uses AI agents to analyze the content  
• Generates structured learning resources  
• Saves the generated documents automatically

This allows users to convert large documents into **useful learning resources instantly**.

---

# Workflow Preview

<img width="872" height="513" alt="Screenshot 2026-03-09 201058" src="https://github.com/user-attachments/assets/6238e7ff-3dd3-4f27-91fe-65a863e4d683" />

---

# How The Workflow Works

The automation is divided into several processing stages.

---

# 1. Detect New Documents

The workflow monitors a specific folder for newly added documents.

When a new file appears, the system automatically begins processing it.

Supported formats include:

• PDF  
• DOCX  
• TXT  

The file is imported and prepared for AI processing.

---

# 2. Extract and Prepare Document Content

The workflow extracts text from the document depending on its type.

Different extraction nodes handle:

• PDF files  
• Word documents  
• Plain text files  

The extracted text is then prepared for AI processing.

---

# 3. Summarization and Vector Storage

The document is summarized and stored in a vector database using embeddings.

This enables **Retrieval Augmented Generation (RAG)**.

Benefits include:

• Efficient knowledge retrieval  
• Context-aware AI responses  
• Improved document understanding  

The workflow uses:

• Mistral embeddings  
• Qdrant vector database  

---

# 4. Generate Study Templates

The workflow automatically generates multiple study resources.

Example outputs include:

### Study Guide
Includes:

• Short-answer quiz questions  
• Answer key  
• Key concepts  
• Glossary of important terms  

---

### Timeline

Creates a chronological list of events found in the document.

Also includes:

• important people  
• contextual descriptions  
• relationships between events  

---

### Briefing Document

A concise overview of the most important insights.

Ideal for:

• quick understanding  
• executive summaries  
• briefing notes

---

# 5. AI Question Generation

The AI agents analyze the summarized document and generate questions to explore its content.

These questions help guide the creation of structured study materials.

The workflow uses multiple AI models to:

• generate questions  
• retrieve relevant information  
• compile answers  
• generate final documents

---

# 6. Generate Final Documents

After processing, the system generates final markdown documents containing the structured notes.

Each template is created automatically.

Example output files:

```
study_guide.md
timeline.md
briefing_doc.md
```

---

# 7. Export Generated Files

The generated documents are exported to the same folder as the original file.

This makes it easy to organize study materials alongside source documents.

---

# Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Mistral AI | Language models |
| Qdrant | Vector database |
| RAG | Knowledge retrieval |
| AI Agents | Content analysis |
| Markdown | Generated output format |

---

# Example Use Cases

This workflow can be used for:

• studying large textbooks  
• converting research papers into notes  
• building knowledge bases  
• training material generation  
• summarizing business documents  
• preparing briefing documents

---



---

# Setup Requirements

To run this workflow you will need:

• n8n instance  
• Mistral API key  
• Qdrant vector database  
• Local folder access for file monitoring

---

# Future Improvements

Possible enhancements:

• support more document formats  
• multi-language support  
• PDF highlighting and annotations  
• integration with Notion or Obsidian  
• knowledge graph generation

---

# Author

Mohammad Alkhatib
