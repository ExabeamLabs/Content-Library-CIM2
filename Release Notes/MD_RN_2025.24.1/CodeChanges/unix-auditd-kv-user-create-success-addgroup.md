# Code Changes for unix-auditd-kv-user-create-success-addgroup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_user', 'host', 'host_ip', 'process_id', 'session_id', 'time'] |
| edit_regex_field | account_name |  | ['\sacct=\"({dest_user}({account_name}[^\"]+))\"'] |
| added_regex_field | dest_user |  | ['\sacct=\"({dest_user}({account_name}[^\"]+))\"'] |
| removed_attribute | DupFields |  | N/A |