# AI-Powered Google Maps Lead Generation

An automated AI lead generation system that extracts business data from Google Maps and enriches it using website scraping and AI processing.

This workflow uses n8n, OpenAI, Apify, and Google Sheets to automatically collect and organize business leads.

---

# Project Overview

This project demonstrates how to build an AI-powered lead generation pipeline capable of:

- Scraping business data from Google Maps
- Extracting company information from websites
- Enriching data using AI
- Storing structured leads automatically in Google Sheets

The system can be used for sales prospecting, marketing campaigns, and business intelligence.

---

# Workflow Preview

<img width="485" height="518" alt="Screenshot 2026-03-09 201906" src="https://github.com/user-attachments/assets/49bf3d44-612e-4db3-a835-48e539f79d60" />


---

# Architecture

The system is composed of multiple workflows that automate lead extraction and enrichment.

---

# 1 AI Lead Generation Agent

The main AI agent receives user requests such as:

Find plumbers in San Francisco

The AI then:

1. Processes the request  
2. Calls the Google Maps scraper  
3. Enriches the results with additional data  
4. Saves the results to Google Sheets  

The agent uses OpenAI to interpret user requests and manage the scraping workflow.

---

# 2 Google Maps Extraction Workflow

This workflow collects business listings using the Apify Google Maps Scraper.

It extracts information such as:

- Business Name  
- Address  
- Phone Number  
- Website  
- Contact Details  

The results are automatically stored inside Google Sheets.

---

# 3 Website Content Crawler

After extracting Google Maps listings, the system can crawl business websites to gather additional information such as:

- Company description  
- Services offered  
- Contact information  
- Website content  

This improves lead quality and provides deeper business insights.

---

# Tech Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| OpenAI | AI reasoning and request processing |
| Apify | Google Maps and website scraping |
| Google Sheets | Lead storage |
| SerpAPI | Fallback data enrichment |
| LangChain Nodes | AI orchestration |

---

# Key Features

- AI-powered lead generation  
- Google Maps business scraping  
- Website data extraction  
- Automated Google Sheets integration  
- AI-assisted enrichment  
- Scalable workflow automation  

---


---

# Setup

To run this workflow you need:

- OpenAI API Key  
- Apify API Token  
- Google Sheets API access  
- n8n environment  

---

# Example Use Cases

This project can be used for:

- Sales lead generation  
- Local business prospecting  
- Market research  
- Competitor analysis  
- CRM data enrichment  

---

# Future Improvements

Possible improvements include:

- Email extraction automation  
- CRM integrations  
- Automatic outreach workflows  
- Lead scoring using AI  
- Real-time business monitoring  

---

# Author

Mohammad Alkhatib
