# Code Changes for microsoft-evsecurity-kv-group-create-success-4731 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'privileges', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({result}(Success|Failure) Audit)\s+({dest_host}({host}[\w\-\.]+))\s+Security Group Management'] |
| edit_regex_field | result |  | ['({result}(Success|Failure) Audit)\s+({dest_host}({host}[\w\-\.]+))\s+Security Group Management'] |
| added_regex_field | dest_host |  | ['({result}(Success|Failure) Audit)\s+({dest_host}({host}[\w\-\.]+))\s+Security Group Management'] |
| removed_attribute | DupFields |  | N/A |