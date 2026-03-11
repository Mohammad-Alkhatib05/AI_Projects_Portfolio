# AI Researcher for Sales

An AI-powered sales research automation system that collects company intelligence from the web and enriches sales data automatically.

This workflow uses **n8n**, **OpenAI**, **SerpAPI**, and **Google Sheets** to research companies, extract key information, and store structured results for sales teams.

---

# Project Overview

This project demonstrates how to build an **AI-powered sales research assistant** capable of:

- Researching companies automatically
- Extracting company data from the web
- Identifying pricing plans and product features
- Detecting integrations and APIs
- Storing structured sales intelligence inside Google Sheets

The system transforms **unstructured company names into structured business insights**.

---

# Workflow Preview

<img width="1136" height="437" alt="Screenshot 2026-03-09 200055" src="https://github.com/user-attachments/assets/b94f19cb-dbf9-4789-8f28-b0bd6ae5fa24" />

---

# Architecture

The workflow automates company research using AI and web search tools.

---

# 1 Workflow Trigger

The workflow can be triggered in two ways:

- Manual trigger for testing
- Scheduled trigger (runs automatically every few hours)

This allows continuous enrichment of sales data.

---

# 2 Retrieve Companies from Google Sheets

The workflow retrieves rows from Google Sheets that require enrichment.

Each row typically contains:

- Company name
- Domain
- Research status

Only rows that need research are processed.

---

# 3 Process Rows Sequentially

The workflow processes company records **one by one** using a loop.

This prevents API rate limits and ensures reliable processing.

---

# 4 AI Company Research Agent

The AI agent researches companies and gathers information such as:

- Company domain
- LinkedIn page
- Market type (B2B or B2C)
- Cheapest pricing plan
- Whether the company offers an API
- Whether a free trial exists
- Enterprise plan availability
- Key integrations
- Latest case study published by the company

The agent uses search tools and website content extraction to gather data.

---

# 5 Web Search and Website Analysis

The workflow gathers company information through:

- Google search using SerpAPI
- Website scraping
- Content extraction from company websites

This allows the AI agent to collect accurate business intelligence.

---

# 6 Structured Data Extraction

The extracted data is formatted using a **Structured Output Parser**.

The AI returns structured JSON data including:

- domain
- linkedinUrl
- market
- cheapest_plan
- has_API
- has_free_trial
- has_enterprise_plan
- integrations
- case_study_link

---

# 7 Update Google Sheets

Finally, the enriched data is written back into **Google Sheets**.

This enables sales teams to maintain an automatically updated lead intelligence database.

---

# Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenAI | AI reasoning and research |
| SerpAPI | Google search automation |
| ScrapingBee | Alternative web scraping |
| Google Sheets | Data storage |
| LangChain Agents | AI orchestration |

---

# Key Features

- AI-powered company research
- Automated sales intelligence collection
- Google search integration
- Website content extraction
- Structured AI output
- Automatic CRM-like enrichment

---


---

# Setup

To run this workflow you need:

- OpenAI API Key
- SerpAPI API Key
- Google Sheets integration
- n8n instance

Optional:

- ScrapingBee API for alternative search scraping.

---

# Example Use Cases

This project can be used for:

- Sales lead enrichment
- Prospect research automation
- Competitive intelligence
- Market analysis
- CRM data enrichment

---

# Future Improvements

Possible improvements include:

- LinkedIn company profile scraping
- CRM integration (HubSpot / Salesforce)
- Email discovery automation
- Lead scoring using AI
- Sales outreach automation

---

# Author

Mohammad Alkhatib
