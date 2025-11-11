# Code Changes for microsoft-evsecurity-kv-group-create-success-4759 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'attribute', 'category', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'new_attribute', 'object', 'old_attribute', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| removed_attribute | DupFields |  | N/A |