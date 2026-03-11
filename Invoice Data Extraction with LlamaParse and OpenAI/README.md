# Invoice Data Extraction with LlamaParse and OpenAI

An AI-powered automation workflow that extracts structured invoice data from PDF attachments using **LlamaParse**, **OpenAI**, and **n8n**.

This system automatically detects invoice emails, processes attached PDF invoices, extracts structured information using AI, and stores the results inside Google Sheets.

---

## Project Overview

This project demonstrates how to build an **AI invoice processing pipeline** that converts unstructured invoice PDFs into structured financial data automatically.

The workflow performs the following tasks:

- Detect incoming invoice emails
- Parse invoice PDFs using LlamaParse
- Extract invoice data using OpenAI
- Save structured results to Google Sheets
- Prevent duplicate invoice processing

This automation is useful for **accounting automation, invoice reconciliation, and financial data processing**.

---

## Workflow Preview

<img width="1115" height="320" alt="Screenshot 2026-03-09 203644" src="https://github.com/user-attachments/assets/93ea7d7e-98a1-4fbb-acde-e5a37ec4bc49" />
<img width="1103" height="358" alt="Screenshot 2026-03-09 211714" src="https://github.com/user-attachments/assets/351348fd-6518-4744-8564-2fa0fa23ba58" />

---

## Architecture

The workflow contains four main stages.

---

## 1. Watch for Invoice Emails

The workflow monitors incoming emails using the Gmail trigger.

Emails are filtered based on:

- Sender email address
- Having a PDF attachment
- Not having the label `invoice synced`

This ensures that only new invoices are processed.

---

## 2. Advanced PDF Processing with LlamaParse

Invoice PDFs are uploaded to **LlamaParse**, a document parsing service by **LlamaIndex Cloud**.

LlamaParse is designed for complex PDFs containing:

- Tables
- Structured invoice line items
- Multi-column layouts
- Embedded objects

Unlike traditional PDF converters, it preserves the document structure which improves extraction accuracy.

---

## 3. Extract Structured Invoice Data with OpenAI

After the invoice is converted into Markdown format, an **OpenAI LLM** extracts structured invoice information.

Extracted fields include:

- Invoice date
- Invoice number
- Purchase order number
- Supplier name
- Supplier address
- Supplier VAT identification number
- Customer name
- Customer address
- Customer VAT identification number
- Shipping addresses
- Line items
- Subtotal without VAT
- Subtotal with VAT
- Total price

The **Structured Output Parser** ensures the AI response is returned as clean JSON.

---

## 4. Store Data in Google Sheets

The extracted invoice data is automatically appended to a **Google Sheets reconciliation sheet**.

This allows finance teams to maintain a structured database of invoices for:

- bookkeeping
- reconciliation
- expense tracking
- financial auditing

---

## 5. Prevent Duplicate Processing

After the invoice is successfully processed, the workflow adds a Gmail label:

```
invoice synced
```

This prevents the same invoice from being processed again.

---

## Tech Stack

| Technology | Purpose |
|-----------|--------|
| n8n | Workflow automation |
| LlamaParse | Advanced PDF parsing |
| OpenAI | AI-powered data extraction |
| Gmail API | Email monitoring |
| Google Sheets | Data storage |
| LlamaIndex Cloud | Document parsing infrastructure |

---


---

## Setup Requirements

To run this workflow you need:

- OpenAI API Key
- LlamaParse API Key
- Gmail integration
- Google Sheets integration
- n8n instance

---

## Example Use Cases

This project can be used for:

- Accounting automation
- Invoice reconciliation
- Financial document processing
- Expense management systems
- ERP integrations
- Document AI pipelines

---

## Future Improvements

Possible improvements include:

- Integration with accounting software (QuickBooks / Xero)
- Invoice validation and fraud detection
- Multi-language invoice support
- OCR fallback for scanned invoices
- Automatic vendor classification

---

## Author

Mohammad Alkhatib
