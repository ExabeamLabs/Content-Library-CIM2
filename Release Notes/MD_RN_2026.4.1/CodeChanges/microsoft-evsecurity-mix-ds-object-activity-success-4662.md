# Code Changes for microsoft-evsecurity-mix-ds-object-activity-success-4662 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'attribute', 'channel', 'domain', 'event_code', 'event_name', 'full_name', 'host', 'login_id', 'object', 'object_name', 'object_server', 'object_type', 'operation', 'properties', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)'] |