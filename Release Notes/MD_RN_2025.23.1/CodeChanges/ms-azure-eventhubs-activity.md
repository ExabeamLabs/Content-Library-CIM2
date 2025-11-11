# Code Changes for ms-azure-eventhubs-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | event_name |  | ['"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"'] |
| edit_regex_field | operation |  | ['"+operationName"+:\s*"+({operation}[^"]+)"+', '"ActivityDisplayName":\s*"({operation}({event_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |