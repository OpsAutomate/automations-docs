# Okta Group <> n8n Project sync

## Problem
Describe the manual and error-prone process that this automation replaces for `Okta Group <> n8n Project sync`.

## Solution
Built an n8n workflow integrating:
- Slack

## Flow
Webhook → Respond to Webhook → Respond → Parsed n8n okta group → Error Trigger → Send a message

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Webhook
- Error Trigger

### Nodes List
| Name | Type |
| --- | --- |
| Webhook | n8n-nodes-base.webhook |
| Respond to Webhook | n8n-nodes-base.respondToWebhook |
| Split Out | n8n-nodes-base.splitOut |
| Respond | n8n-nodes-base.respondToWebhook |
| Parsed n8n okta group | n8n-nodes-base.code |
| Sticky Note | n8n-nodes-base.stickyNote |
| Error Trigger | n8n-nodes-base.errorTrigger |
| Send a message | n8n-nodes-base.slack |
| n8n Okta Group wtih Role | n8n-nodes-base.httpRequest |
| Get n8n User ID search | n8n-nodes-base.httpRequest |
| Filter email | n8n-nodes-base.filter |
| Sticky Note1 | n8n-nodes-base.stickyNote |
