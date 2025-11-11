# Code Changes for microsoft-defenderep-sk4-endpoint-activity-deviceevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | category |  | ['category"+:\s*"+({event_name}({category}[^"]+))'] |
| edit_regex_field | event_name |  | ['ActionType"+:\s*"+({event_name}[^"]+)', 'category"+:\s*"+({event_name}({category}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |