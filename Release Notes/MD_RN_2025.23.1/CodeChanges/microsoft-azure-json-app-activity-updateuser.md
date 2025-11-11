# Code Changes for microsoft-azure-json-app-activity-updateuser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['"ActivityDisplayName":\s*"({event_name}[^"]+)"', '"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"'] |
| edit_regex_field | operation |  | ['"+operationName"+:\s*"+({operation}[^"]+)"+', '"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |