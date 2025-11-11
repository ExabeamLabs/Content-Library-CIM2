# Code Changes for microsoft-o365-json-app-login-graphsignin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['email_address', 'event_name', 'full_name', 'operation', 'user'] |
| edit_regex_field | event_name |  | ['exa_regex=({operation}({event_name}Sign-In))'] |
| added_regex_field | operation |  | ['exa_regex=({operation}({event_name}Sign-In))'] |
| removed_attribute | DupFields |  | N/A |