# Code Changes for microsoft-evsecurity-xml-password-read-5379-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'channel', 'domain', 'event_code', 'event_id', 'host', 'login_id', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |