# Code Changes for microsoft-evsecurity-xml-process-create-success-4688 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'dest_user', 'domain', 'event_code', 'event_name', 'full_name', 'host', 'login_id', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'service_name', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |