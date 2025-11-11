# Code Changes for microsoft-defenderep-cef-endpoint-notification-advancehuntingdevinfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | category |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| edit_regex_field | event_name |  | ['ActionType":\s*"({event_name}[^"]+)', 'category"+:\s*"+({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |