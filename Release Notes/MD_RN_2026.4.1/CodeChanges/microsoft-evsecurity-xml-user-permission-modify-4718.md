# Code Changes for microsoft-evsecurity-xml-user-permission-modify-4718 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_removed_right', 'access_type', 'channel', 'domain', 'event_code', 'host', 'login_id', 'process_id', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |