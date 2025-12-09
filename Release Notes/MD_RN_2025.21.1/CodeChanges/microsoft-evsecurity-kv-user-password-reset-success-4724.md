# Code Changes for microsoft-evsecurity-kv-user-password-reset-success-4724 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'result', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+))\s+ADAuditPlus'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+))\s+ADAuditPlus'] |
| removed_attribute | DupFields |  | N/A |