# Code Changes for microsoft-evsecurity-xml-group-modify-success-4750 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'privileges', 'process_id', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |