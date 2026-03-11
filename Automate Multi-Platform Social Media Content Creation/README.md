# Automate Multi-Platform Social Media Content Creation

An AI-powered automation system that generates, approves, and publishes social media content across multiple platforms automatically.

This workflow uses **AI agents, n8n automation, and platform APIs** to create optimized content for different social networks and publish them from a single pipeline.

---

## Project Overview

This project demonstrates how to build an **AI Social Media Content Factory** capable of generating and publishing content across multiple platforms automatically.

The system can:

- Generate social media posts using AI
- Adapt content for different platforms
- Generate images automatically
- Request approval before publishing
- Publish content across multiple platforms
- Archive generated posts and assets

Supported platforms include:

- X (Twitter)
- Instagram
- Facebook
- LinkedIn
- Threads
- YouTube Shorts

---

## Workflow Preview

<img width="872" height="513" alt="Screenshot 2026-03-09 201058" src="https://github.com/user-attachments/assets/40602779-8aa7-4ad8-9108-098378ac34c7" />

---

## Architecture Overview

The automation system is divided into multiple components.

---

## 1. Social Media Router Agent

The workflow starts when a user submits a content request.

An AI agent determines:

- Which platform the content is for
- What type of content should be generated
- Which tool or workflow should handle the request

The agent routes the request to the correct publishing pipeline.

---

## 2. Social Media Content Factory

The content factory generates platform-specific posts using AI.

It dynamically builds prompts using:

- System prompt configuration
- Platform-specific schema
- User content request

The AI then generates structured content including:

- Post text
- Caption
- Call-to-action
- Hashtags
- Image suggestions

---

## 3. Image Generation

The workflow generates a matching image for the post using an AI image generator.

Steps include:

- Generating an image prompt
- Creating the image automatically
- Uploading the image to a hosting service
- Saving the image to Google Drive

This ensures every post includes visual content.

---

## 4. Content Approval Step

Before publishing, the system sends the generated post for approval.

Approval can be done through email or messaging services.

This allows human review before publishing content automatically.

---

## 5. Publish to Social Media Platforms

Once approved, the workflow publishes content to multiple platforms.

Supported platforms include:

### X (Twitter)
Short and concise posts optimized for engagement.

### Instagram
Visual content posts with captions and hashtags.

### Facebook
Community-focused posts encouraging interaction.

### LinkedIn
Professional posts focused on business insights.

### Threads
Discussion-based social posts designed for engagement.

### YouTube Shorts
Short-form video content suggestions.

Each platform receives content optimized for its specific audience and algorithm.

---

## 6. Archive Content

The workflow archives generated assets including:

- Social media post text
- Image assets
- Metadata
- JSON structured content

All assets are stored in **Google Drive** for future reuse and tracking.

---

## 7. Notification and Reporting

The system can optionally send notifications when content is generated or published.

Notifications may include:

- Email reports
- Messaging notifications
- Debug or status updates

---

## Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenAI / LLMs | AI content generation |
| Pollinations AI | Image generation |
| Google Drive | Content storage |
| Gmail | Approval and notifications |
| Social Media APIs | Publishing content |
| Telegram (optional) | Notifications |

---



---

## Setup Requirements

To run this workflow you need:

- OpenAI API Key
- Social media platform credentials
- Google Drive integration
- Gmail integration
- n8n instance

Optional:

- Telegram Bot API for notifications
- Image hosting API

---

## Example Use Cases

This system can be used for:

- Marketing automation
- Social media scheduling
- Brand content automation
- AI content generation pipelines
- Creator productivity tools
- Startup marketing automation

---

## Future Improvements

Possible improvements include:

- Content scheduling
- Analytics integration
- Engagement tracking
- Automatic hashtag optimization
- Multi-language content generation

---

## Author

Mohammad Alkhatib
