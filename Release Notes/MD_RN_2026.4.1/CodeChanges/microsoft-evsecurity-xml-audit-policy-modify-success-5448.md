# Code Changes for microsoft-evsecurity-xml-audit-policy-modify-success-5448 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'channel', 'event_code', 'event_id', 'host', 'operation', 'process_guid', 'process_id', 'provider_name', 'result', 'run_level', 'sub_category', 'time', 'user_sid'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |