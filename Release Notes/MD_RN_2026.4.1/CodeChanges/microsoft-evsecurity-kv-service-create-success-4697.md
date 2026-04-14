# Code Changes for microsoft-evsecurity-kv-service-create-success-4697 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'result', 'service_command_line', 'service_name', 'service_start_type', 'service_type', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |