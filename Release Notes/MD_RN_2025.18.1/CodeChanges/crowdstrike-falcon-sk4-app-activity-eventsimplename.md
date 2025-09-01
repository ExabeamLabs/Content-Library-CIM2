# Code Changes for crowdstrike-falcon-sk4-app-activity-eventsimplename (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['app-activity:success', 'endpoint-command:success', 'process-create:success', 'registry-modify:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'process-created', 'registry-write'] |