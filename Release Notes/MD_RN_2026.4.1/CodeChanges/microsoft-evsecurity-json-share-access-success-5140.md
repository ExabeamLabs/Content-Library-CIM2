# Code Changes for microsoft-evsecurity-json-share-access-success-5140 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'channel', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'file_type', 'host', 'login_id', 'process_id', 'service_name', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |