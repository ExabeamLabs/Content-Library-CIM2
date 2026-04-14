# Code Changes for microsoft-evsecurity-xml-endpoint-notification-success-4876 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'thread_id', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |