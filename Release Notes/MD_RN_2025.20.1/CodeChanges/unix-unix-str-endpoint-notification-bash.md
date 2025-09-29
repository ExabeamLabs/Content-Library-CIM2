# Code Changes for unix-unix-str-endpoint-notification-bash (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'host', 'process_id', 'process_name', 'time'] |
| edit_regex_field | process_id |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+', 'bash\[({process_id}\d+)\]:\s*({additional_info}.+?)\s*$'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s+'] |