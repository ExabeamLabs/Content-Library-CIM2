# Code Changes for microsoft-evsecurity-json-service-create-success-4697 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'operation_type', 'process_id', 'result', 'service_command_line', 'service_name', 'service_start_type', 'service_type', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |