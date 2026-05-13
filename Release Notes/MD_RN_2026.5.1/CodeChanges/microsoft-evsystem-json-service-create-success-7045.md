# Code Changes for microsoft-evsystem-json-service-create-success-7045 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'channel', 'dest_host', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'service_command_line', 'service_name', 'service_type', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |