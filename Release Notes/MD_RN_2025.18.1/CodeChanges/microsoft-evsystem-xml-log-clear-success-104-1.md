# Code Changes for microsoft-evsystem-xml-log-clear-success-104-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'<\/"]+)'] |