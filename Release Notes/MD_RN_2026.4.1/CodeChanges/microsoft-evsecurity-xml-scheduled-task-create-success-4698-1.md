# Code Changes for microsoft-evsecurity-xml-scheduled-task-create-success-4698-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'arg', 'author', 'channel', 'description', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type_text', 'process_dir', 'process_name', 'process_path', 'run_level', 'src_domain', 'src_user', 'task_name', 'time', 'triggers', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |