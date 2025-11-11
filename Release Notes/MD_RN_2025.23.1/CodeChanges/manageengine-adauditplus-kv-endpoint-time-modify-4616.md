# Code Changes for manageengine-adauditplus-kv-endpoint-time-modify-4616 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+)) ADAuditPlus'] |
| removed_attribute | DupFields |  | N/A |