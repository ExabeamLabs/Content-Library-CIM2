# Code Changes for microsoft-evntlm-xml-endpoint-login-success-8002 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'domain', 'event_code', 'event_name', 'host', 'login_type', 'process_dir', 'process_name', 'process_path', 'run_level', 'src_host', 'src_ip', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |