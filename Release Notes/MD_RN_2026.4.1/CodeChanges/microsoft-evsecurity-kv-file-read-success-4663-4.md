# Code Changes for microsoft-evsecurity-kv-file-read-success-4663-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'additional_info', 'category', 'channel', 'domain', 'event_code', 'event_name', 'file_dir', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'registry_key', 'registry_path', 'src_domain', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['\schannel="+({channel}[^"]+)"'] |