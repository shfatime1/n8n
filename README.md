# Job Application Automation (n8n Workflow)

This repository contains an advanced **n8n** workflow designed to automate the job application, analysis, and communication process using Large Language Models (LLMs) and AI Agents.

## 🚀 Project Overview

This automation system orchestrates the intake of applicant data, retrieves supporting documentation, and utilizes an AI Agent to evaluate or draft personalized responses before sending out confirmation emails. It minimizes manual overhead by handling repetitive data processing tasks automatically.

## 🛠️ How It Works (Workflow Structure)

The workflow consists of the following automated steps:

1. **Google Sheets Trigger (`rowAdded`):** Automatically fires the workflow whenever a new job application row is added to a tracking spreadsheet.
2. **Google Docs Integration (`Get a document`):** Fetches relevant documentation (such as a CV or a custom application response) dynamically.
3. **Basic LLM Chain (`OpenRouter Chat Model`):** Processes the initial raw data and structures the context using advanced language models via OpenRouter.
4. **AI Agent (`OpenRouter Chat Model 2` + `Simple Memory` + `Code Tool`):** A smart conversational agent equipped with memory to maintain context and a Python/JavaScript custom code execution tool to evaluate applications or structure data intelligently.
5. **Gmail Integration (`Send a message`):** Automatically dispatches a tailored, professional email notification or response back to the recipient based on the AI Agent's output.

## 💻 Setup and Installation

To import this workflow into your own n8n instance:

1. Download the `Job Application Automation.json` file from this repository.
2. Log into your n8n dashboard and create a new blank workflow.
3. Click on the top-right menu icon (three dots) and select **Import from File**, then upload the downloaded JSON file.
4. Configure your credentials for the following nodes:
   * **Google Sheets & Google Docs** (OAuth2 authentication)
   * **OpenRouter** (API Key for your preferred LLM model)
   * **Gmail** (OAuth2 authentication)
5. Set the workflow status to **Active** (Publish).
