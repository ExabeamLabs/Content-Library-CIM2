# Code Changes for microsoft-evsecurity-kv-endpoint-activity-success-4665 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'audit_category', 'channel', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'result_code', 'time', 'user', 'user_sid'] |
| added_regex_field | channel |  | ['Channel="({channel}[^"]+)', 'Channel="({channel}[^"]+)'] |