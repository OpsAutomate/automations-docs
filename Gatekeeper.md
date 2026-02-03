# Gatekeeper

## Problem
Describe the manual and error-prone process that this automation replaces for `Gatekeeper`.

## Solution
Built an n8n workflow integrating:
- Google Workspace
- Slack

## Flow
/gatekeeper → Get information about a user → Code in JavaScript → No data → Webhook → Respond to Webhook

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- /gatekeeper
- Webhook

### Nodes List
| Name | Type |
| --- | --- |
| /gatekeeper | n8n-nodes-base.webhook |
| Get information about a user | n8n-nodes-base.slack |
| Code in JavaScript | n8n-nodes-base.code |
| No data | n8n-nodes-base.respondToWebhook |
| If | n8n-nodes-base.if |
| Webhook | n8n-nodes-base.webhook |
| Respond to Webhook | n8n-nodes-base.respondToWebhook |
| Switch | n8n-nodes-base.switch |
| Access Request Modal | n8n-nodes-base.httpRequest |
| Denied Message | n8n-nodes-base.httpRequest |
| Check user if not exist on group | n8n-nodes-base.httpRequest |
| Assign Okta Admin | n8n-nodes-base.httpRequest |
| Success | n8n-nodes-base.httpRequest |
| Wait | n8n-nodes-base.wait |
| Revoke access | n8n-nodes-base.httpRequest |
| Notify: Access Revoked | n8n-nodes-base.httpRequest |
| Sticky Note | n8n-nodes-base.stickyNote |
| HTTP Request | n8n-nodes-base.httpRequest |
| Add user to group | n8n-nodes-base.gSuiteAdmin |
| route | n8n-nodes-base.switch |
| Remove user from group | n8n-nodes-base.gSuiteAdmin |
| Sticky Note1 | n8n-nodes-base.stickyNote |
| Sticky Note2 | n8n-nodes-base.stickyNote |
