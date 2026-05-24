# AI-Driven Job Application Tracking & Fault-Tolerant Pipeline

An automated, asynchronous backend data pipeline built in n8n that ingests unstructured incoming emails, classifies application status metrics using an LLM, and routes the status into a comprehensive tracking sheet. ALso added real-time system diagnostics using a Discord operations bot.

## 🛠️ Architecture Overview
* **Data Ingestion:** Automatically polls incoming email data once a day.
* **AI Classification:** Formulates semantic status states (Applied, Interview, Offer, Rejected) from unstructured text bodies.
* **Relevancy check:** Checks for relevancy in a validation loop and appends every relevant and irrelevant mail data to corresponding sheet.
* **Logging:** Logs Date, Job title, Company Name, Status, Reason for the status in the sheet.
* **Fault Tolerance:** A decoupled Global Error Handling sub-workflow intercepts runtime exceptions via an independent trigger framework.

## 📂 Repository Structure
* `job-application-tracker.json` - Main data processing and classification blueprint.
* `global-error-handler.json` - Global error catching and Discord API router.

## 🚀 How To Import
1. Create a new workflow canvas inside your n8n instance.
2. Click the top-right menu -> **Import from File**.
3. Upload `job-application-tracker.json` and configure your local credentials (Google, OpenRouter).

<img width="2196" height="813" alt="image" src="https://github.com/user-attachments/assets/b438c7e4-eeee-4954-83f3-17bfd55b6ffb" />

