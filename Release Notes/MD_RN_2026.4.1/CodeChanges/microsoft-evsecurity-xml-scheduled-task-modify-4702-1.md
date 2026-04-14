# Code Changes for microsoft-evsecurity-xml-scheduled-task-modify-4702-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'arg', 'author', 'channel', 'description', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'result', 'run_level', 'src_host', 'task_name', 'time', 'triggers', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |