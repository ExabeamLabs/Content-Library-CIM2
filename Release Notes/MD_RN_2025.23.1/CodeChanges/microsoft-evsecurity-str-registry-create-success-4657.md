# Code Changes for microsoft-evsecurity-str-registry-create-success-4657 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'handle_id', 'host', 'login_id', 'old_registry_details', 'old_registry_details_type', 'operation', 'process_dir', 'process_id', 'process_name', 'process_path', 'registry_details', 'registry_details_type', 'registry_key', 'registry_path', 'registry_value', 'result', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['<Computer>({src_host}({host}[\w\-.]+?))<\/Computer>', 'ComputerName=({src_host}({host}[^\s]+))', '\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(\d{4}|({src_host}({host}[\w\-.]+)))\s\w+'] |
| added_regex_field | src_host |  | ['<Computer>({src_host}({host}[\w\-.]+?))<\/Computer>', 'ComputerName=({src_host}({host}[^\s]+))', '\w+\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s(\d{4}|({src_host}({host}[\w\-.]+)))\s\w+'] |
| removed_attribute | DupFields |  | N/A |