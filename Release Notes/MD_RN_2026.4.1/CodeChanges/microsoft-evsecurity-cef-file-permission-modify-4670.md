# Code Changes for microsoft-evsecurity-cef-file-permission-modify-4670 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'new_attribute', 'object_id', 'object_name', 'object_type', 'old_attribute', 'process_dir', 'process_id', 'process_name', 'process_path', 'resource', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |