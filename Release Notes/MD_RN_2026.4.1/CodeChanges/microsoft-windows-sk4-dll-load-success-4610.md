# Code Changes for microsoft-windows-sk4-dll-load-success-4610 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'channel', 'domain', 'event_code', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'log_source', 'login_id', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['Channel":"({channel}[^"]+)'] |