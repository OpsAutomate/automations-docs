# MeetSync-cebu_manager

## Problem
Describe the manual and error-prone process that this automation replaces for `MeetSync-cebu_manager`.

## Solution
Built an n8n workflow integrating:
- Google Workspace

## Flow
Check Cebu Availability → Book Cebu Calendar → Log to Google Sheets → Return Busy Msg → Return Success Msg → When Executed by Another Workflow → ...

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- When Executed by Another Workflow

### Nodes List
| Name | Type |
| --- | --- |
| Check Cebu Availability | n8n-nodes-base.googleCalendar |
| Is Room Free? | n8n-nodes-base.if |
| Book Cebu Calendar | n8n-nodes-base.googleCalendar |
| Log to Google Sheets | n8n-nodes-base.googleSheets |
| Return Busy Msg | n8n-nodes-base.respondToWebhook |
| Return Success Msg | n8n-nodes-base.respondToWebhook |
| Edit Fields | n8n-nodes-base.set |
| When Executed by Another Workflow | n8n-nodes-base.executeWorkflowTrigger |
| AI Agent | @n8n/n8n-nodes-langchain.agent |
| Append or update row in sheet in Google Sheets | n8n-nodes-base.googleSheetsTool |
| Search Logs | n8n-nodes-base.googleSheetsTool |
| Delete | n8n-nodes-base.googleCalendarTool |
| Update | n8n-nodes-base.googleCalendarTool |
| Simple Memory | @n8n/n8n-nodes-langchain.memoryBufferWindow |
| OpenAI Chat Model | @n8n/n8n-nodes-langchain.lmChatOpenAi |
| If | n8n-nodes-base.if |
| Return Update/Cancel Msg | n8n-nodes-base.respondToWebhook |
| Get All Events | n8n-nodes-base.googleCalendarTool |
| Unique ID Generate | n8n-nodes-base.code |
| Code in JavaScript | n8n-nodes-base.code |
| Switch | n8n-nodes-base.switch |
