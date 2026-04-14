# Code Changes for windows-system-info (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'audit_category', 'channel', 'event_code', 'event_id', 'login_id', 'result_code', 'user_sid'] |
| added_regex_field | channel |  | ['Channel="({channel}[^"]+)'] |