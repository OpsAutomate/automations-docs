# EndCycle_Step 1 - Offboarding Notifcation

## Problem
Describe the manual and error-prone process that this automation replaces for `EndCycle_Step 1 - Offboarding Notifcation`.

## Solution
Built an n8n workflow integrating:
- Google Workspace
- Slack

## Flow
Gmail Trigger → Google Gemini Chat Model → Webhook → Respond to Webhook → Code in JavaScript → Delete a message → ...

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Gmail Trigger
- Webhook

### Nodes List
| Name | Type |
| --- | --- |
| Gmail Trigger | n8n-nodes-base.gmailTrigger |
| Edit Fields | n8n-nodes-base.set |
| Information Extractor | @n8n/n8n-nodes-langchain.informationExtractor |
| Google Gemini Chat Model | @n8n/n8n-nodes-langchain.lmChatGoogleGemini |
| If | n8n-nodes-base.if |
| Sticky Note | n8n-nodes-base.stickyNote |
| No Operation, do nothing | n8n-nodes-base.noOp |
| Webhook | n8n-nodes-base.webhook |
| Respond to Webhook | n8n-nodes-base.respondToWebhook |
| Code in JavaScript | n8n-nodes-base.code |
| Switch | n8n-nodes-base.switch |
| Delete a message | n8n-nodes-base.slack |
| Confirmed | n8n-nodes-base.slack |
| logs | n8n-nodes-base.googleSheets |
| Reject | n8n-nodes-base.slack |
| Request Confirmation before Proceed | n8n-nodes-base.slack |
| Sticky Note1 | n8n-nodes-base.stickyNote |
