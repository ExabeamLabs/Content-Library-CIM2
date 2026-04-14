# Code Changes for microsoft-evsecurity-xml-endpoint-authentication-4774 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'channel', 'domain', 'event_code', 'event_name', 'host', 'run_level', 'time', 'user', 'user_type'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |