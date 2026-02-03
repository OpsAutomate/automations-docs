# EndCycle_Step 2 - Unsuspend User in GW - Schedule Trigger

## Problem
Describe the manual and error-prone process that this automation replaces for `EndCycle_Step 2 - Unsuspend User in GW - Schedule Trigger`.

## Solution
Built an n8n workflow integrating:
- Google Workspace
- Slack

## Flow
Google Sheets Trigger → Update row in sheet → Send a message

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Google Sheets Trigger

### Nodes List
| Name | Type |
| --- | --- |
| Google Sheets Trigger | n8n-nodes-base.googleSheetsTrigger |
| Get a user | n8n-nodes-base.gSuiteAdmin |
| Update User UnSuspend | n8n-nodes-base.httpRequest |
| Sticky Note1 | n8n-nodes-base.stickyNote |
| Move User to ex_Users OU | n8n-nodes-base.httpRequest |
| Suspended? | n8n-nodes-base.if |
| Sticky Note2 | n8n-nodes-base.stickyNote |
| Update row in sheet | n8n-nodes-base.googleSheets |
| approve_action | n8n-nodes-base.filter |
| Send a message | n8n-nodes-base.slack |
