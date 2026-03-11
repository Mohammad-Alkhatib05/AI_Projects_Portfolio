# Competitor Pricing Change Monitor

An automated competitor pricing monitoring system that tracks changes on competitors’ pricing pages and instantly notifies you when differences are detected.

This workflow continuously scans pricing pages, compares them with previously recorded pricing data, and alerts you when competitors modify their prices or pricing structures.

---

# Project Overview

Monitoring competitor pricing manually is time-consuming and error-prone, especially for SaaS companies or e-commerce businesses with complex pricing tiers.

This automation solves the problem by creating a fully automated monitoring pipeline.

The system:

• Reads competitor pricing page URLs from Google Sheets  
• Extracts pricing information automatically  
• Compares current pricing with historical pricing  
• Detects significant pricing changes  
• Logs updated pricing data  
• Sends alerts when differences are found  

This allows businesses to **react quickly to market pricing changes** and adjust their strategy accordingly.

The workflow uses an AI extraction system to analyze pricing pages and detect meaningful changes. :contentReference[oaicite:0]{index=0}

---

# Workflow Preview

<img width="722" height="527" alt="Screenshot 2026-03-09 213029" src="https://github.com/user-attachments/assets/0d505665-1548-4877-bdf2-0c4f783c0b92" />


---

# How The Workflow Works

The automation runs through several stages to detect pricing changes.

---

# 1. Trigger Workflow

The workflow can be triggered manually or scheduled to run periodically.

Once triggered, the automation begins scanning competitor pricing pages.

---

# 2. Load Competitor URLs

Competitor pricing page URLs are stored inside a Google Sheets document.

The workflow reads the sheet and retrieves:

• competitor pricing page URLs  
• previously recorded pricing data  
• row identifiers used for updates  

This sheet acts as the central database for monitoring competitors.

---

# 3. Extract Pricing Information

Each pricing page is analyzed automatically using an AI extraction node.

The system extracts:

• pricing plan names  
• price values  
• key features included in each plan  

It generates a structured summary describing the pricing model.

Example extracted output:

Pricing summary  
Differences summary  
Status flag indicating whether the pricing has changed

---

# 4. Compare With Previous Pricing

The extracted pricing is compared against previously stored pricing information.

The system identifies whether the pricing is:

NEW — pricing was not previously stored  
SIMILAR — pricing remains unchanged  
DIFF — pricing has significantly changed  

Only meaningful differences trigger notifications.

---

# 5. Filter Unchanged Pricing

A filtering step removes results that are marked as **SIMILAR**.

This prevents unnecessary notifications and ensures only real changes are reported.

---

# 6. Update Pricing History

When a pricing change is detected, the system updates the Google Sheet.

The sheet stores:

• latest pricing summary  
• timestamp of the scan  
• pricing page URL  

This creates a historical record of competitor pricing.

---

# 7. Send Notification

If a pricing difference is detected, the workflow sends a notification to Slack.

The notification contains:

• the pricing page URL  
• a summary of pricing differences  

This enables teams to respond immediately to competitor changes.

---

# Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| Airtop AI | Pricing page extraction |
| Google Sheets | Pricing data storage |
| Slack | Change notifications |
| AI Extraction | Pricing analysis |

---

# Example Use Cases

This automation can be used for:

• SaaS competitor price monitoring  
• e-commerce price tracking  
• competitive intelligence systems  
• market research automation  
• pricing strategy monitoring  

---

# Setup Requirements

To run this workflow you will need:

• n8n instance  
• Airtop API key  
• Google Sheets account  
• Slack workspace for alerts  
• list of competitor pricing page URLs  

---

# Future Improvements

Possible improvements include:

• tracking feature changes across plans  
• adding email or Telegram notifications  
• monitoring promotional pricing changes  
• generating automated competitor analysis reports  
• visualizing historical pricing trends  

---

# Author

Mohammad Alkhatib
