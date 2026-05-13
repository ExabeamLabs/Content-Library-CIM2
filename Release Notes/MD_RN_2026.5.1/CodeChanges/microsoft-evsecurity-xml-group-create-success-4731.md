# Code Changes for microsoft-evsecurity-xml-group-create-success-4731 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |