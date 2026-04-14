# Code Changes for microsoft-evsecurity-xml-group-modify-success-4735-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_name', 'group_id', 'group_name', 'host', 'login_id', 'process_id', 'result', 'run_level', 'src_domain', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |