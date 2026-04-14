# Code Changes for microsoft-evsecurity-xml-scheduled-task-disable-4701-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'author', 'channel', 'description', 'dest_host', 'domain', 'event_code', 'host', 'login_id', 'login_type_text', 'run_level', 'src_domain', 'src_user', 'task_name', 'thread_id', 'time', 'triggers', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |