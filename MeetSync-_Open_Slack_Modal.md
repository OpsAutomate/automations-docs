# MeetSync- Open Slack Modal

## Problem
Describe the manual and error-prone process that this automation replaces for `MeetSync- Open Slack Modal`.

## Solution
Built an n8n workflow integrating:
- Slack

## Flow
Webhook → Slack Data → Interactivity → Submission Payload → Get Info User → AI Response → ...

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Webhook
- Interactivity
- Slack Trigger

### Nodes List
| Name | Type |
| --- | --- |
| Webhook | n8n-nodes-base.webhook |
| Slack Data | n8n-nodes-base.code |
| Sticky Note | n8n-nodes-base.stickyNote |
| AI Agent | @n8n/n8n-nodes-langchain.agent |
| OpenAI Chat Model | @n8n/n8n-nodes-langchain.lmChatOpenAi |
| Simple Memory | @n8n/n8n-nodes-langchain.memoryBufferWindow |
| cebu_manager | @n8n/n8n-nodes-langchain.toolWorkflow |
| Action Selection | n8n-nodes-base.httpRequest |
| Interactivity | n8n-nodes-base.webhook |
| Book | n8n-nodes-base.httpRequest |
| Route based on Action | n8n-nodes-base.switch |
| Update | n8n-nodes-base.httpRequest |
| Cancel | n8n-nodes-base.httpRequest |
| Submission Payload | n8n-nodes-base.code |
| Get Info User | n8n-nodes-base.slack |
| If | n8n-nodes-base.if |
| Denied | n8n-nodes-base.httpRequest |
| AI Response | n8n-nodes-base.code |
| Confirm | n8n-nodes-base.httpRequest |
| Sticky Note1 | n8n-nodes-base.stickyNote |
| Switch | n8n-nodes-base.switch |
| No Data | n8n-nodes-base.respondToWebhook |
| No Operation, do nothing | n8n-nodes-base.noOp |
| Back to Selection1 | n8n-nodes-base.httpRequest |
| Slack Trigger | n8n-nodes-base.slackTrigger |
| HTTP Request | n8n-nodes-base.httpRequest |
| No Operation, do nothing1 | n8n-nodes-base.noOp |
| App_Home_Opened? | n8n-nodes-base.if |
| Sticky Note2 | n8n-nodes-base.stickyNote |
| Respond to Webhook | n8n-nodes-base.respondToWebhook |
| manila_manager | @n8n/n8n-nodes-langchain.toolWorkflow |
| Structured Output Parser | @n8n/n8n-nodes-langchain.outputParserStructured |
