# Code Changes for microsoft-windows-xml-endpoint-authentication-fail-adfs342 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'event_code', 'event_id', 'failure_reason', 'host', 'process_id', 'run_level', 'thread_id', 'time', 'user_id', 'user_sid', 'user_upn'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |