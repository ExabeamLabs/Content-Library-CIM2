# Code Changes for microsoft-evsystem-xml-service-create-success-7045 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'arg', 'channel', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'run_level', 'service_name', 'service_type', 'src_host', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |