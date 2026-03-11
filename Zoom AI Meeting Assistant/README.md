# Zoom AI Meeting Assistant

An AI-powered workflow that automatically processes Zoom meetings, generates meeting summaries, creates tasks, schedules follow-up meetings, and sends structured email reports.

This automation uses **Zoom**, **AI models**, **ClickUp**, and **Microsoft Outlook** to turn meeting transcripts into actionable outcomes.

---

## Project Overview

This project demonstrates how to build an **AI meeting assistant** that analyzes Zoom meeting transcripts and automatically performs post-meeting tasks.

The workflow automatically:

- Retrieves the latest Zoom meeting
- Downloads the meeting transcript
- Generates structured meeting minutes using AI
- Creates tasks in ClickUp
- Schedules follow-up meetings in Outlook
- Sends a formatted meeting summary via email

This is useful for **team productivity, meeting documentation, and workflow automation**.

---

## Workflow Preview

<img width="1021" height="405" alt="Screenshot 2026-03-09 213128" src="https://github.com/user-attachments/assets/133455a2-da11-4b64-ba6a-f50a444aea47" />

---

## Workflow Architecture

The workflow processes meetings in several stages.

---

## 1. Retrieve Latest Zoom Meeting

The workflow starts with a trigger and retrieves data from the latest Zoom meetings.

It filters meetings that occurred within the **last 24 hours** to ensure only recent meetings are processed.

---

## 2. Retrieve Meeting Transcript

The workflow retrieves transcript data from the Zoom API.

Steps include:

- Fetch meeting recordings
- Locate transcript files
- Download the transcript
- Extract readable text from the transcript

If no transcript exists, the workflow stops to avoid errors.

---

## 3. Prepare Transcript for AI Processing

The raw transcript is cleaned and formatted to remove timestamps and unnecessary formatting.

This produces a structured text transcript that can be processed by an AI model.

---

## 4. Generate AI Meeting Summary

An AI model analyzes the meeting transcript and produces a structured meeting report including:

- Meeting title and date
- Participants
- Summary of the discussion
- Action items
- Important deadlines

The AI converts the transcript into **structured meeting minutes**.

---

## 5. Create Tasks Automatically

The AI analyzes the transcript to identify actionable tasks.

Tasks are automatically created in **ClickUp**, including:

- Task name
- Description
- Due date
- Priority
- Project name

This ensures that action items discussed during meetings are automatically tracked.

---

## 6. Schedule Follow-Up Meetings

If the transcript mentions future meetings, the system automatically schedules a follow-up meeting in **Microsoft Outlook Calendar**.

Information extracted includes:

- Meeting title
- Date and time
- Participants

---

## 7. Generate Email Summary

The AI-generated meeting summary is converted into an **HTML email report**.

The email includes:

- Meeting title
- List of participants
- Summary of the meeting
- Tasks created
- Important dates

---

## 8. Send Meeting Summary Email

Finally, the workflow sends the formatted meeting summary to participants via email.

This ensures that everyone receives a clear summary of the meeting and next steps.

---

## Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Zoom API | Meeting data and transcripts |
| AI Model (Anthropic/OpenAI) | Meeting analysis |
| ClickUp | Task management |
| Microsoft Outlook | Calendar scheduling |
| SMTP / Email | Sending meeting summaries |

---


---

## Setup Requirements

To run this workflow you need:

- Zoom API credentials
- AI model API (OpenAI / Anthropic / Ollama)
- ClickUp API access
- Microsoft Outlook integration
- SMTP email configuration
- n8n instance

---

## Example Use Cases

This automation can be used for:

- Meeting documentation
- Automated meeting minutes
- Task extraction from meetings
- Project management automation
- Follow-up meeting scheduling
- Productivity automation

---

## Future Improvements

Possible improvements include:

- Slack or Teams notifications
- Automatic CRM updates
- Meeting sentiment analysis
- Speaker detection
- Multi-language transcript processing

---

## Author

Mohammad Alkhatib
