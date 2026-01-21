# CRM Data Q&A Agent

[![Stars](https://img.shields.io/github/stars/vladkol/crm-data-agent?style=flat-square)](https://github.com/vladkol/crm-data-agent/stargazers)
[![Forks](https://img.shields.io/github/forks/vladkol/crm-data-agent?style=flat-square)](https://github.com/vladkol/crm-data-agent/network)
[![License](https://img.shields.io/github/license/vladkol/crm-data-agent?style=flat-square)](https://github.com/vladkol/crm-data-agent/blob/main/LICENSE)
[![Language](https://img.shields.io/github/languages/top/vladkol/crm-data-agent?style=flat-square)](https://github.com/vladkol/crm-data-agent)

CRM Data Q&A Agent an advanced **AI-powered analytics and BI agent** that lets you interact with CRM data using natural language and retrieves insights with automated SQL queries. Built for Salesforce data replicated into BigQuery, this project shows how to combine retrieval-augmented generation (RAG), NL2SQL, and visualization for business intelligence workflows. :contentReference[oaicite:0]{index=0}

---

## Overview

CRM Data Q&A Agent turns your CRM data into an intelligent, conversational analytics engine. Instead of writing SQL or building dashboards manually, you simply ask questions in plain language like “Who are our top 5 customers by revenue?” and the agent answers with insights and visualizations powered by SQL queries generated on the fly. :contentReference[oaicite:1]{index=1}

This gives users a way to quickly explore business performance without deep technical expertise, leveraging large language models (LLMs), query generation, and contextual AI workflows.

---

## Problem

Modern CRM systems store massive volumes of CRM data accounts, contacts, opportunities, tasks, and more but:

- 🔹 Business users struggle to extract insights without SQL knowledge.  
- 🔹 Traditional BI tools require complex setup and maintenance.  
- 🔹 Static dashboards can’t answer new or unexpected questions.  
- 🔹 Analysts spend too much time hand-coding queries instead of delivering insights.  

This makes timely, flexible data exploration difficult for non-technical stakeholders.

---

## Solution

CRM Data Q&A Agent bridges the gap between business users and data by:

- **Natural Language Interfaces:** Users ask questions in plain English.  
- **Automated NL2SQL:** The agent generates SQL queries against a replicated BigQuery dataset of Salesforce data.  
- **Dynamic Insights & Visuals:** Results can be returned as data tables or Vega-Lite charts, giving immediate insights.  
- **Multi-Agent RAG Workflow:** Uses an advanced retrieval-augmented generation pipeline with context and multi-agent orchestration.  
- **Build on ADK:** It’s built with the Agent Development Kit (ADK), a modular framework for AI agents. :contentReference[oaicite:2]{index=2}

---

## Results & Impact

With CRM Data Q&A Agent:

- Report creation time is reduced from hours to minutes.  
- Non-technical teams can explore CRM trends using plain language.  
- BI workflows become more interactive and responsive to business needs.  
- Teams gain the ability to generate ad-hoc visual analytics without specialized BI skills.  
- It enables smarter, data-driven decisions across sales and marketing functions.

---

## Architecture

CRM Data Q&A Agent integrates several modern components and architectural layers:

- **Data Source:** Salesforce data replicated to Google BigQuery.  
- **AI Workflow:** Retrieval-Augmented Generation (RAG) with long-context handling using Gemini 2.5 Pro.
![image alt](https://github.com/Mutahar1/CRM-Data-QA-Agent/blob/25a0ed444500ce4f76fc7df543ab299ced083045/screenshot-dark.png)

- **NL2SQL Engine:** Translates natural language questions into precise SQL queries.  
- **Analytics Layer:** Executes SQL against BigQuery and returns structured results.
  ![image alt](https://github.com/Mutahar1/CRM-Data-QA-Agent/blob/25a0ed444500ce4f76fc7df543ab299ced083045/data_agent_design.jpg)

- **Visualization:** Optional Vega-Lite chart generation for graphs and dashboards.

- **Agent Development Kit (ADK):** Provides the modular framework for agents, session services, and event streaming. :contentReference[oaicite:3]{index=3}
  
  ![image alt](https://github.com/Mutahar1/CRM-Data-QA-Agent/blob/25a0ed444500ce4f76fc7df543ab299ced083045/top_5_customers.jpg)

---

## Tech Stack

CRM Data Q&A Agent primarily uses:

- **Python** — Core language for agents and orchestration. :contentReference[oaicite:4]{index=4}  
- **BigQuery** — Cloud data warehouse storing replicated Salesforce tables. :contentReference[oaicite:5]{index=5}  
- **Google Cloud Services:**  
  - Vertex AI — Model hosting and execution. :contentReference[oaicite:6]{index=6}  
  - Firestore — Session management. :contentReference[oaicite:7]{index=7}  
- **ADK (Agent Development Kit)** — Multi-agent framework. :contentReference[oaicite:8]{index=8}  
- **Vega-Lite** — Visualization specification for interactive charts. :contentReference[oaicite:9]{index=9}  
- **Streamlit** (optional UI example) — Web UI for interacting with the agent. :contentReference[oaicite:10]{index=10}

---

## How to Deploy & Run

### Requirements

Before deploying, ensure you have:

- Google Cloud Project with billing enabled  
- BigQuery dataset loaded with Salesforce data  
- AI Storage Bucket and Firestore database  
- Vertex AI permissions configured  
- Python 3.11 or later installed

---

### Manual Installation

1. **Clone the repo:**
   ```bash
   git clone https://github.com/vladkol/crm-data-agent.git
   cd crm-data-agentpython -m venv .venv
source .venv/bin/activate
pip install -r src/requirements.txt
gcloud services enable \
  aiplatform.googleapis.com \
  firestore.googleapis.com \
  bigquery.googleapis.com \
  run.googleapis.com \
  cloudbuild.googleapis.com \
  --project=$GOOGLE_CLOUD_PROJECT
./deploy_to_cloud_run.sh
./run_local.sh
CRM Data Q&A Agent — an advanced **AI-powered analytics and BI agent** that lets you interact with CRM data using natural language and retrieves insights with automated SQL queries. Built for Salesforce data replicated into BigQuery, this project shows how to combine retrieval-augmented generation (RAG), NL2SQL, and visualization for business intelligence workflows. :contentReference[oaicite:0]{index=0}

---
### License

This project is licensed under the Apache 2.0 License.
