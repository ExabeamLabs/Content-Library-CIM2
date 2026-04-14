# Code Changes for microsoft-evsecurity-xml-group-modify-success-4737-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_id', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'privileges', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |