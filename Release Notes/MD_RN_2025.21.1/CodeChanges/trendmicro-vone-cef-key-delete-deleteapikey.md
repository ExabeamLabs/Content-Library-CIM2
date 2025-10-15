# Code Changes for trendmicro-vone-cef-key-delete-deleteapikey (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'category', 'event_category', 'event_code', 'event_name', 'full_name', 'host', 'key_name', 'operation', 'result', 'role', 'time', 'user'] |
| edit_regex_field | event_name |  | [' cs3=({operation}({event_name}[^=]+?))((\s+\w+=)|\s*$)'] |
| added_regex_field | operation |  | [' cs3=({operation}({event_name}[^=]+?))((\s+\w+=)|\s*$)'] |
| removed_attribute | DupFields |  | N/A |