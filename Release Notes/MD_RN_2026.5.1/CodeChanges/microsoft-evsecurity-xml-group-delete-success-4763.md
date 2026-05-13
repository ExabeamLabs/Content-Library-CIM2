# Code Changes for microsoft-evsecurity-xml-group-delete-success-4763 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_id', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'process_id', 'run_level', 'src_domain', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |