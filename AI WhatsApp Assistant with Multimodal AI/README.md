# AI WhatsApp Assistant with Multimodal AI

An AI-powered WhatsApp assistant capable of understanding and responding to **text, images, audio, and video messages** using modern multimodal AI models.

The system uses **n8n**, **Google Gemini**, and an **AI Agent** to process incoming WhatsApp messages and generate intelligent responses automatically. :contentReference[oaicite:0]{index=0}

---

# Project Overview

This project demonstrates how to build a **multimodal WhatsApp AI chatbot** that can:

- Receive messages from WhatsApp users
- Detect the message type (text, image, audio, video)
- Process the message using AI models
- Generate an intelligent response
- Send the response back to the user automatically

The workflow is built using **n8n automation** and an **AI Agent architecture**. :contentReference[oaicite:1]{index=1}

---

# Workflow Preview

<img width="1115" height="477" alt="Screenshot 2026-03-09 203140" src="https://github.com/user-attachments/assets/b2647b04-cd40-4523-b616-40c807598d8a" />


---

# Architecture

The system processes WhatsApp messages through multiple AI pipelines depending on the message type.

---

# 1 WhatsApp Trigger

The workflow starts when a user sends a message on WhatsApp.

The WhatsApp Trigger node receives the incoming message and passes it into the workflow for processing. :contentReference[oaicite:2]{index=2}

---

# 2 Message Type Detection

The system automatically detects the message type and routes it into different processing branches:

- Audio messages
- Video messages
- Image messages
- Text messages

Each branch processes the content using the appropriate AI model. :contentReference[oaicite:3]{index=3}

---

# 3 Audio Message Processing

For audio messages or voice notes:

1. The audio file is downloaded
2. Google Gemini transcribes the audio
3. The transcription is passed to the AI Agent

This allows the chatbot to understand voice messages.

---

# 4 Video Message Processing

For video messages:

1. The video is downloaded
2. Google Gemini analyzes the video content
3. A description of the video is generated
4. The AI Agent uses this description to generate a response

---

# 5 Image Message Analysis

For image messages:

1. The image is downloaded
2. A multimodal AI model analyzes the image
3. The system extracts descriptions or text from the image

This enables the chatbot to understand visual content.

---

# 6 Text Message Processing

For text messages:

1. The text is summarized
2. The processed message is passed to the AI Agent

This improves response quality and understanding.

---

# 7 AI Agent Response

The AI Agent processes the user's request and generates an intelligent response.

The system uses:

- Google Gemini Chat Model
- Memory buffer for conversation history
- External knowledge tools such as Wikipedia

This enables the chatbot to provide informative and contextual responses. :contentReference[oaicite:4]{index=4}

---

# 8 Send Response to User

Finally, the system sends the generated response back to the WhatsApp user automatically.

The WhatsApp node can send:

- Text messages
- Images
- Audio
- Video
- Documents
- Location

---

# Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| WhatsApp API | Messaging integration |
| Google Gemini | Multimodal AI processing |
| AI Agent | Response generation |
| Wikipedia Tool | Knowledge retrieval |

---

# Key Features

- Multimodal AI chatbot
- Supports text, image, audio, and video messages
- Automatic message processing
- AI-generated responses
- Conversation memory
- Automated WhatsApp replies

---

  

---

# Setup

To run this workflow you need:

- WhatsApp API access
- Google Gemini API key
- n8n environment
- Webhook configuration

---

# Example Use Cases

This system can be used for:

- Customer support automation
- AI assistants for businesses
- Automated FAQ responses
- Multimodal chatbot applications
- AI help desks

---

# Future Improvements

Possible improvements include:

- CRM integration
- Appointment booking automation
- Voice response generation
- Multi-language support
- AI knowledge base integration

---

# Author

Mohammad Alkhatib
