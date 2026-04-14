# Code Changes for microsoft-evsecurity-xml-endpoint-logout-4647-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_domain', 'dest_user', 'event_code', 'event_id', 'host', 'login_id', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'thread_id', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |