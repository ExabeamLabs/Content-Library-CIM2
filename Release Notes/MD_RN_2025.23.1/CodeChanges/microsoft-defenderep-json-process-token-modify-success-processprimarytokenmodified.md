# Code Changes for microsoft-defenderep-json-process-token-modify-success-processprimarytokenmodified (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | action |  | ['ActionType":\s*"({operation}({action}[^"]+))'] |
| edit_regex_field | category |  | ['category":\s*"({event_name}({category}[^"]+))'] |
| edit_regex_field | event_name |  | ['"tokenChangeDescription\\*":\\*"({event_name}[^"]+)\\*"', 'category":\s*"({event_name}({category}[^"]+))'] |
| edit_regex_field | operation |  | ['ActionType":\s*"({operation}({action}[^"]+))', 'operationName":\s*"({operation}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |