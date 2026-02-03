# AssetOps Slack Admin Only

## Problem
Describe the manual and error-prone process that this automation replaces for `AssetOps Slack Admin Only`.

## Solution
Built an n8n workflow integrating:
- Google Workspace
- Slack

## Flow
Get information about a user → Menu → slack slash command → Extract Payload → Prepare Google Docs Data → Download file → ...

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Menu
- slack slash command
- Request (Download Signed PDF)
- Webhook

### Nodes List
| Name | Type |
| --- | --- |
| Get information about a user | n8n-nodes-base.slack |
| If | n8n-nodes-base.if |
| Employee Dashboard | n8n-nodes-base.noOp |
| Menu | n8n-nodes-base.webhook |
| slack slash command | n8n-nodes-base.webhook |
| Extract Payload | n8n-nodes-base.code |
| Cebu Menu | n8n-nodes-base.httpRequest |
| Copy Automated IT Accountability Template | n8n-nodes-base.httpRequest |
| Prepare Google Docs Data | n8n-nodes-base.code |
| Download file | n8n-nodes-base.googleDrive |
| Upload file | n8n-nodes-base.googleDrive |
| Update Template (assign user assets) | n8n-nodes-base.httpRequest |
| Send a message | n8n-nodes-base.slack |
| Docusign | n8n-nodes-base.httpRequest |
| Covert to Base64 for Docusign | n8n-nodes-base.code |
| Docusign Notification to the team | n8n-nodes-base.slack |
| Request (Download Signed PDF) | n8n-nodes-base.webhook |
| Upload Signed | n8n-nodes-base.googleDrive |
| Send final confirmation | n8n-nodes-base.slack |
| Get Envelope Recipient | n8n-nodes-base.httpRequest |
| Prepare transfer to Drive | n8n-nodes-base.httpRequest |
| Sticky Note | n8n-nodes-base.stickyNote |
| Select Site | n8n-nodes-base.httpRequest |
| Manila Menu | n8n-nodes-base.httpRequest |
| Switch | n8n-nodes-base.switch |
| form_submitted Selected Site | n8n-nodes-base.switch |
| selected_site Form | n8n-nodes-base.switch |
| Automated IT Accountability Template Manila | n8n-nodes-base.httpRequest |
| Prepare Google Doc Data Manila | n8n-nodes-base.code |
| Update Template (assign user assets) Manila | n8n-nodes-base.httpRequest |
| Respond to Docusign  | n8n-nodes-base.respondToWebhook |
| Respond to Slack command and Menu | n8n-nodes-base.respondToWebhook |
| Sticky Note1 | n8n-nodes-base.stickyNote |
| Webhook | n8n-nodes-base.webhook |
| Respond to Monday | n8n-nodes-base.respondToWebhook |
| Copy Manila Monday Accountability Form | n8n-nodes-base.httpRequest |
| Update Template (assign user assets) ManilaMonday | n8n-nodes-base.httpRequest |
| Prepare Monday data to Docs | n8n-nodes-base.code |
| Has data? | n8n-nodes-base.if |
| Sticky Note2 | n8n-nodes-base.stickyNote |
| Extract Monday | n8n-nodes-base.code |
| Covert to Base64 for Docusign from Monday | n8n-nodes-base.code |
| DL File | n8n-nodes-base.googleDrive |
| Monday Docusign | n8n-nodes-base.httpRequest |
| Unavailable | n8n-nodes-base.httpRequest |
