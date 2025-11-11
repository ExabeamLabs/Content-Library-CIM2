# Code Changes for microsoft-evsecurity-kv-group-member-remove-success-removedfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'group_name', 'group_type', 'host', 'login_id', 'src_host', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| removed_attribute | DupFields |  | N/A |