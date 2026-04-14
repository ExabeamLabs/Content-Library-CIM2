# Code Changes for microsoft-evsecurity-json-process-create-success-4688-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_command_line', 'process_dir', 'process_guid', 'process_name', 'process_path', 'src_domain', 'src_host', 'src_user', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |