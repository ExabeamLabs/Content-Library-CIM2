# Code Changes for microsoft-defenderep-json-network-notification-success-networkinfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | category |  | ['"Type"+:\s*"+({event_name}({category}[^",]+))'] |
| edit_regex_field | event_name |  | ['"Type"+:\s*"+({event_name}({category}[^",]+))', 'Type"+:"+({event_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |