# Code Changes for microsoft-evsecurity-xml-certificate-request-fail-4888 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['attributes', 'channel', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'sub_category', 'thread_id', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |