# Code Changes for cisco-cucm-kv-app-activity-success-useraccess (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | ['EventStatus =', 'EventType =UserAccess', 'ResourceAccessed='] | [' %UC_AUDITLOG-', '=UserAccess', 'EventStatus', 'EventType', 'ResourceAccessed='] |