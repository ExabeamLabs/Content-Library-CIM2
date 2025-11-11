# Code Changes for microsoft-evsecurity-xml-registry-create-success-4657 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_id', 'full_name', 'host', 'login_id', 'object_id', 'old_registry_details', 'old_registry_details_type', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'registry_details', 'registry_details_type', 'registry_key', 'registry_path', 'registry_value', 'result', 'run_level', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[^\<]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| added_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[^\<]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({dest_host}({host}[\w_\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |