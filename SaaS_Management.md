# SaaS Management Suite

## Problem
IT and Procurement teams often struggle with decentralized SaaS visibility. Manually checking user lists and owners across dozens of platforms (AWS, GitHub, Slack, etc.) is time-consuming and prone to human error, specially during audits or offboarding.

## Solution
Built an advanced **AI-Powered SaaS Assistant** in Slack. It uses an AI Agent to interpret natural language requests and dynamically calls specialized "Tools" (sub-workflows) to fetch live data.
- **AI Agent (Google Gemini)**: Interprets context (e.g., "who has access to loom?").
- **Modular Tools**: Over 10+ sub-workflows for apps like AWS, GitHub, Monday, Google, and more.
- **Slack Interface**: Threaded responses with formatted summaries and departmental breakdowns.

## Flow
Slack Trigger → Add Reaction → AI Agent (Gemini) → [Dynamic Tool Call] → Tool Results → Send Response to Slack Thread

## Result
Centralizes SaaS governance into a single chat interface. Reduces the time to verify application access from minutes to seconds, providing IT teams with an effortless "Source of Truth" in Slack.

## Technical Details
### Triggers
- **Slack Trigger**: Mentions or messages in the SaaS Management workspace.

### Integrations & Tools
This suite connects to the following through modular sub-workflows:
- **Cloud/IDP**: AWS, JumpCloud, Google Workspace.
- **Dev/Product**: GitHub, Unleash, Pendo, MixMax.
- **Collab**: Monday.com, Loom, Miro, Notion, Slack.

### Main Nodes List
| Name | Type |
| --- | --- |
| Slack Trigger | n8n-nodes-base.slackTrigger |
| AI Agent | @n8n/n8n-nodes-langchain.agent |
| Google Gemini Chat Model | @n8n/n8n-nodes-langchain.lmChatGoogleGemini |
| Simple Memory | @n8n/n8n-nodes-langchain.memoryBufferWindow |
| Tool Callers | @n8n/n8n-nodes-langchain.toolWorkflow |
| Send a message | n8n-nodes-base.slack |
