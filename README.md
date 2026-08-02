# 🧾 AI Telegram Invoice Extractor Agent (Make.com Automation)

An automated AI Telegram Bot built on **Make.com** that accepts invoice photos or PDF files directly from Telegram, extracts invoice details using **AI OCR Document Processing**, logs structured data into **Google Sheets**, and replies with an instant summary back to the user.

---

## 🔗 Quick Links

- **🚀 Make.com Shared Scenario (1-Click Import):** [Clone Scenario on Make.com](https://us2.make.com/public/shared-scenario/SyhefzqLTHO/invoice-extractor-agent)
- **📦 GitHub Repository:** [https://github.com/ThecrashO/make-telegram-invoice-extractor](https://github.com/ThecrashO/make-telegram-invoice-extractor)

---

## 🔄 Workflow Architecture

1. **Trigger:** `Telegram (Watch Updates)` - Listens for incoming photos or PDF invoice attachments sent to the Telegram Bot.
2. **File Download:** `Telegram (Download a File)` - Downloads the invoice image/document using the file ID.
3. **AI Document Extraction:** `Make AI Extractors (Extract Information from an Invoice)` - Parses the file using OCR AI to extract Vendor Name, Invoice ID, Invoice Date, Total Amount, and Currency.
4. **Data Logging:** `Google Sheets (Add a Row)` - Records the structured invoice details into Google Sheets.
5. **Instant Notification:** `Telegram (Send Reply Message)` - Replies back to the user on Telegram with a clean confirmation summary.

---

## ✨ Key Features

- **Mobile-First & Convenient:** Allows field staff and accountants to submit receipts/invoices directly via Telegram.
- **Smart File Handling:** Supports both **PDF documents** and **Image/Photo** invoice uploads.
- **AI OCR Extraction:** Automatically reads Vendor Name, Invoice Number, Issue Date, Total Amount, and Currency without manual typing.
- **Automated Expense Tracking:** Logs clean, structured data directly into Google Sheets.
- **Instant Confirmation:** Sends a confirmation summary back to the user on Telegram instantly.

---

## 📊 Google Sheet Column Setup

Ensure your Google Sheet contains the following headers in **Row 1** (Columns A to H):

| Column A | Column B | Column C | Column D | Column E | Column F | Column G | Column H |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Processed Date** | **Vendor Name** | **Invoice Number** | **Invoice Date** | **Total Amount** | **Currency** | **Submitted By** | **Telegram Chat ID** |

---

## 🛠️ Prerequisites

- **Make.com Account**
- **Telegram Bot Token** (from `@BotFather`)
- **Google Sheets Connection**
- **Make AI Extractors Connection**

---

## 🚀 How to Import & Setup on Make.com

### Method 1: 1-Click Import (Recommended)
1. Open the Make.com Shared Scenario link provided above.
2. Click **Clone Scenario** to import it directly into your workspace.

### Method 2: Manual Blueprint Import
1. Download `Telegram Invoice Extractor Agent.blueprint.json` from this repository.
2. In **Make.com**, create a new scenario and select **Import Blueprint** (from the three dots menu at the bottom toolbar).
3. Upload `Telegram Invoice Extractor Agent.blueprint.json`.

---

## ⚙️ Configuration Steps

1. **Setup Telegram Connection:**
   - Connect your **Telegram Bot Webhook** (Module 1) and **Telegram Connection** (Modules 2 & 5).
2. **Setup Google Sheets Connection:**
   - Connect your **Google Account** in Module 4 and select your destination spreadsheet.
3. Turn **ON** the scenario schedule.

---
