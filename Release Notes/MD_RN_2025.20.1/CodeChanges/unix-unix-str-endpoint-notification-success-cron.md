# Code Changes for unix-unix-str-endpoint-notification-success-cron (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'host', 'process_command_line', 'process_id', 'process_name', 'time'] |
| added_regex_field | process_id |  | ['\s+.*\/({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+.*\/({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |