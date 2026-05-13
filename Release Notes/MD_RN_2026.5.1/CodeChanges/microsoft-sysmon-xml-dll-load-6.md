# Code Changes for microsoft-sysmon-xml-dll-load-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_id', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_signature', 'file_signature_status', 'file_signed', 'hash_md5', 'host', 'log_name', 'operation', 'result', 'run_level', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |