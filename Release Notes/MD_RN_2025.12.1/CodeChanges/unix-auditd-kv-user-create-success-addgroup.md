# Code Changes for unix-auditd-kv-user-create-success-addgroup (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | ['op=add-group', 'res=success', 'type=ADD_GROUP'] | ['ADD_GROUP', 'op=add-group', 'res=success'] |