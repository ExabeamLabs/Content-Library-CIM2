# Code Changes for microsoft-windows-sk4-group-list-success-4798 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'log_source', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['Channel":"({channel}[^"]+)'] |