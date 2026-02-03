# Step 4 - Google Account Step - Schedule Trigger

## Problem
Describe the manual and error-prone process that this automation replaces for `Step 4 - Google Account Step - Schedule Trigger`.

## Solution
Built an n8n workflow integrating:
- Google Workspace

## Flow
Extract ID's → Get AFI Back up Completed → Schedule Trigger → Get row(s) in sheet → Update row in sheet

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Schedule Trigger

### Nodes List
| Name | Type |
| --- | --- |
| Get Employee for File Transfer | n8n-nodes-base.gSuiteAdmin |
| Execute Transfer to Manager | n8n-nodes-base.httpRequest |
| Get Transfer Status | n8n-nodes-base.httpRequest |
| Wait | n8n-nodes-base.wait |
| Merge | n8n-nodes-base.merge |
| Extract ID's | n8n-nodes-base.code |
| Get Manager for File Transfer | n8n-nodes-base.gSuiteAdmin |
| Get Apps to Transfer | n8n-nodes-base.httpRequest |
| Get AFI Back up Completed | n8n-nodes-base.code |
| Schedule Trigger | n8n-nodes-base.scheduleTrigger |
| Get row(s) in sheet | n8n-nodes-base.googleSheets |
| If | n8n-nodes-base.if |
| No Operation, do nothing | n8n-nodes-base.noOp |
| Update row in sheet | n8n-nodes-base.googleSheets |
