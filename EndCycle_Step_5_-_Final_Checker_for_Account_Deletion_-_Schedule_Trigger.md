# EndCycle_Step 5 - Final Checker for Account Deletion - Schedule Trigger

## Problem
Describe the manual and error-prone process that this automation replaces for `EndCycle_Step 5 - Final Checker for Account Deletion - Schedule Trigger`.

## Solution
Built an n8n workflow integrating:
- Google Workspace
- Slack

## Flow
Update Sheet → Send Notification  → Schedule Trigger → Backup Statuses Validation → Get Offboarding Sheet Data

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Schedule Trigger

### Nodes List
| Name | Type |
| --- | --- |
| Update Sheet | n8n-nodes-base.googleSheets |
| Send Email To Manager | n8n-nodes-base.gmail |
| Delete a user | n8n-nodes-base.gSuiteAdmin |
| Send Notification  | n8n-nodes-base.slack |
| Schedule Trigger | n8n-nodes-base.scheduleTrigger |
| Backup Statuses Validation | n8n-nodes-base.code |
| If | n8n-nodes-base.if |
| No Operation, do nothing | n8n-nodes-base.noOp |
| Get Offboarding Sheet Data | n8n-nodes-base.googleSheets |
