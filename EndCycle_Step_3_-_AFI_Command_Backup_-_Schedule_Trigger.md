# EndCycle_Step 3 - AFI Command Backup - Schedule Trigger

## Problem
Describe the manual and error-prone process that this automation replaces for `EndCycle_Step 3 - AFI Command Backup - Schedule Trigger`.

## Solution
Built an n8n workflow integrating:
- Google Workspace
- Slack

## Flow
Get row(s) in sheet → Send a message → Schedule Trigger → Update GW Status and AFI Status → Get GW Activated

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Schedule Trigger

### Nodes List
| Name | Type |
| --- | --- |
| Sticky Note | n8n-nodes-base.stickyNote |
| Filter | n8n-nodes-base.filter |
| Get User | n8n-nodes-base.httpRequest |
| Get Resource | n8n-nodes-base.httpRequest |
| get AFI resource_id | n8n-nodes-base.set |
| Get row(s) in sheet | n8n-nodes-base.googleSheets |
| Get Protections | n8n-nodes-base.httpRequest |
| Split Protections | n8n-nodes-base.splitOut |
| Split Resources | n8n-nodes-base.splitOut |
| Filter by Resource ID | n8n-nodes-base.filter |
| Trigger the Job (Backup) to get the Job ID | n8n-nodes-base.httpRequest |
| Get Task and Status | n8n-nodes-base.httpRequest |
| Send a message | n8n-nodes-base.slack |
| Schedule Trigger | n8n-nodes-base.scheduleTrigger |
| If | n8n-nodes-base.if |
| No Operation, do nothing | n8n-nodes-base.noOp |
| Set Email | n8n-nodes-base.set |
| Split Out | n8n-nodes-base.splitOut |
| Limit | n8n-nodes-base.limit |
| Update GW Status and AFI Status | n8n-nodes-base.googleSheets |
| Get GW Activated | n8n-nodes-base.code |
| Wait | n8n-nodes-base.wait |
