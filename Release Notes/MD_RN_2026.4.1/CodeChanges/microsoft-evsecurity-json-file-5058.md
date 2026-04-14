# Code Changes for microsoft-evsecurity-json-file-5058 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'category', 'channel', 'dest_host', 'domain', 'event_code', 'event_name', 'file_path', 'host', 'key_name', 'log_source', 'login_id', 'operation', 'process_guid', 'process_id', 'result', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |