# Code Changes for microsoft-azure-sk4-app-activity-adduser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"'] |
| edit_regex_field | operation |  | ['"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"', '({operation}Add user)'] |
| removed_attribute | DupFields |  | N/A |