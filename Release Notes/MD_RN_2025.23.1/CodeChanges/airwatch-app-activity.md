# Code Changes for airwatch-app-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'domain', 'email_address', 'event_name', 'operation', 'time', 'user'] |
| edit_regex_field | event_name |  | ['Event Type:\s*({operation}({event_name}[^=]+?))\s*User:'] |
| added_regex_field | operation |  | ['Event Type:\s*({operation}({event_name}[^=]+?))\s*User:'] |
| removed_attribute | DupFields |  | N/A |