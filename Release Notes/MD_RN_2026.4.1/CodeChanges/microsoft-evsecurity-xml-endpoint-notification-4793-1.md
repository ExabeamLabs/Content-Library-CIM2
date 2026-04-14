# Code Changes for microsoft-evsecurity-xml-endpoint-notification-4793-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'src_domain', 'src_host', 'src_host_windows', 'src_user', 'sub_category', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |