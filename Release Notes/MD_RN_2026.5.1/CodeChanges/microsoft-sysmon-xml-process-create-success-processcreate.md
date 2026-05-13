# Code Changes for microsoft-sysmon-xml-process-create-success-processcreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'domain', 'event_code', 'hash_md5', 'hash_sha256', 'host', 'login_id', 'parent_process_command_line', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_integrity', 'process_name', 'process_path', 'result', 'run_level', 'src_host', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |