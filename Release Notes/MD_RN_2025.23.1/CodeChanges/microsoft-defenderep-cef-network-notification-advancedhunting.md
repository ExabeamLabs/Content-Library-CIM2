# Code Changes for microsoft-defenderep-cef-network-notification-advancedhunting (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | category |  | ['category"+:\s*"+({category}[^"]+)', 'category"+:\s*"+({event_name}({category}[^"]+))'] |
| edit_regex_field | event_name |  | ['category"+:"+({event_name}[^"]+)', 'category"+:\s*"+({event_name}({category}[^"]+))'] |