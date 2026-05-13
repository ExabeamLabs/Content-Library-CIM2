# Code Changes for microsoft-sysmon-xml-process-create-success-processcreate-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_process_dir', 'dest_process_id', 'dest_process_name', 'dest_process_path', 'domain', 'hash_md5', 'host', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'src_host', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |