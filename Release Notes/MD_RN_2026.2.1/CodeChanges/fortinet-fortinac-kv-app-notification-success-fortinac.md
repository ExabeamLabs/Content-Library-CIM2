# Code Changes for fortinet-fortinac-kv-app-notification-success-fortinac (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | category |  | ['cat="?({category}[^=]+?)"?(\s+\w+=|$)'] |