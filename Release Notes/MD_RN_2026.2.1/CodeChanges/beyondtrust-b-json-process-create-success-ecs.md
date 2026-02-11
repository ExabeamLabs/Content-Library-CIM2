# Code Changes for beyondtrust-b-json-process-create-success-ecs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_attribute | end_timeFormat |  | N/A |
| changed | Conditions |  | ['"EPMWinMac":', '"Type":"Process', '"agent":', '"code":"', 'AgentEventAudit'] |
| edit_attribute | activity_type |  | ['process-create:fail', 'process-create:success'] |
| edit_attribute | legacy_activity_type |  | ['process-created', 'process-created-failed'] |