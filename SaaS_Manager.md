# SaaS Manager

## Problem
Searching for SaaS application details (owners, renewal dates, and pricing) is currently a manual process involving navigating through multiple Monday.com boards or spreadsheets, leading to delays in procurement and management decisions.

## Solution
Built an intelligent n8n workflow that acts as a Slack bot, allowing users to query app information directly. It integrates:
- **Slack**: For user interaction and triggering.
- **LangChain (Google Gemini)**: To intelligently extract app names from natural language queries.
- **Monday.com API**: To fetch and process structured data from centralized boards.

## Flow
Slack Trigger → Information Extractor (Gemini) → Monday.com Request → Collector (Pagination) → Data Processing → Search/Match → Send to Slack

## Result
Provides instant access to application metadata, reducing search time for IT and Procurement teams and ensuring high-stake renewal dates are never missed.

## Technical Details
### Triggers
- **Slack Trigger**: Activates on app mentions or specific messages in watched workspaces.

### Nodes List
| Name | Type |
| --- | --- |
| Slack Trigger | n8n-nodes-base.slackTrigger |
| Add a reaction | n8n-nodes-base.slack |
| Information Extractor | @n8n/n8n-nodes-langchain.informationExtractor |
| Google Gemini Chat Model | @n8n/n8n-nodes-langchain.lmChatGoogleGemini |
| Monday.com Request | n8n-nodes-base.httpRequest |
| Collector | n8n-nodes-base.code |
| Monday.com Loop | n8n-nodes-base.httpRequest |
| Data Processing | n8n-nodes-base.code |
| Search/Match | n8n-nodes-base.code |
| Send a message | n8n-nodes-base.slack |
