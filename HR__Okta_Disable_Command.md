# HR <> Okta Disable Command

## Problem
Describe the manual and error-prone process that this automation replaces for `HR <> Okta Disable Command`.

## Solution
Built an n8n workflow integrating:
- Okta
- Slack

## Flow
Webhook → Get information about a user → Get a user → Denied Message(Non-HR) → Successful → Respond to Webhook → ...

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Webhook
- Slack Get UserEmail

### Nodes List
| Name | Type |
| --- | --- |
| Webhook | n8n-nodes-base.webhook |
| Get information about a user | n8n-nodes-base.slack |
| If | n8n-nodes-base.if |
| Get a user | n8n-nodes-base.okta |
| Denied Message | n8n-nodes-base.slack |
| Successful | n8n-nodes-base.slack |
| Respond to Webhook | n8n-nodes-base.respondToWebhook |
| Show Menu | n8n-nodes-base.httpRequest |
| Slack Get UserEmail | n8n-nodes-base.webhook |
| Respond to Slack | n8n-nodes-base.respondToWebhook |
| Code in JavaScript | n8n-nodes-base.code |
| Get information about a user1 | n8n-nodes-base.slack |
| Deactivate | n8n-nodes-base.httpRequest |
