# Code Changes for sailpoint-identityiq-json-app-activity-success-appactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'app', 'email_address', 'event_name', 'operation', 'time', 'user', 'user_dn', 'user_ou'] |
| edit_regex_field | operation |  | ['"ACTION\\?":\\?"({event_name}({operation}[^"]+?))\\?"'] |
| added_regex_field | event_name |  | ['"ACTION\\?":\\?"({event_name}({operation}[^"]+?))\\?"'] |