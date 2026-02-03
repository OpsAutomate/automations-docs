# Stuck Workflow in Guesty n8n

## Problem
Describe the manual and error-prone process that this automation replaces for `Stuck Workflow in Guesty n8n`.

## Solution
Built an n8n workflow integrating:
- Google Workspace
- Slack

## Flow
Code in JavaScript → Append row in sheet → Code in JavaScript1 → Merge Workflow ID and Workflow name → Notify in Slack → Reduce Workflow Payload → ...

## Result
Describe the business impact and efficiency gains (e.g., time saved, error reduction) achieved with this automation.

## Technical Details
### Triggers
- Schedule Trigger

### Nodes List
| Name | Type |
| --- | --- |
| HTTP Request | n8n-nodes-base.httpRequest |
| Code in JavaScript | n8n-nodes-base.code |
| Split Out | n8n-nodes-base.splitOut |
| Append row in sheet | n8n-nodes-base.googleSheets |
| Code in JavaScript1 | n8n-nodes-base.code |
| Get Project | n8n-nodes-base.httpRequest |
| Merge Workflow ID and Workflow name | n8n-nodes-base.code |
| Notify in Slack | n8n-nodes-base.slack |
| Reduce Workflow Payload | n8n-nodes-base.code |
| summary | n8n-nodes-base.splitInBatches |
| Merge | n8n-nodes-base.merge |
| Send Done Confirmation | n8n-nodes-base.slack |
| Final Count | n8n-nodes-base.code |
| Schedule Trigger | n8n-nodes-base.scheduleTrigger |
