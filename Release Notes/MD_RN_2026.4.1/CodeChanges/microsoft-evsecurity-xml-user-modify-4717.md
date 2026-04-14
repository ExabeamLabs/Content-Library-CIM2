# Code Changes for microsoft-evsecurity-xml-user-modify-4717 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_granted_right', 'access_type', 'channel', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_id', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |