# Code Changes for microsoft-defenderep-json-endpoint-notification-advancehuntingdevinfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | action |  | ['ActionType":\s*"({operation}({action}[^"]+))', 'exa_regex=operationName":\s*"({action}[^"]+)'] |
| edit_regex_field | category |  | ['category":\s*"({event_name}({category}[^"]+))'] |
| edit_regex_field | event_name |  | ['category":\s*"({event_name}({category}[^"]+))', 'exa_regex=ActionType":\s*"({event_name}[^"]+)'] |
| edit_regex_field | operation |  | ['ActionType":\s*"({operation}({action}[^"]+))', 'operationName":\s*"({operation}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | Platform |  | ['MacOS', 'Microsoft Defender', 'Unix', 'Windows'] |