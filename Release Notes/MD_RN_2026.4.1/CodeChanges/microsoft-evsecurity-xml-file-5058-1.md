# Code Changes for microsoft-evsecurity-xml-file-5058-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'key_name', 'key_type', 'login_id', 'operation', 'return_code', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |