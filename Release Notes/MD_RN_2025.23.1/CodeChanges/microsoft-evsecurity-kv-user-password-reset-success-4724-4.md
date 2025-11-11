# Code Changes for microsoft-evsecurity-kv-user-password-reset-success-4724-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'domain', 'error_code', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'registry_key', 'registry_path', 'result', 'service_type', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s|;)'] |
| added_regex_field | dest_host |  | ['Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s|;)'] |
| removed_attribute | DupFields |  | N/A |