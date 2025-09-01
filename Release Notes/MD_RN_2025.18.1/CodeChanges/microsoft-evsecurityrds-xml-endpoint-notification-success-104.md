# Code Changes for microsoft-evsecurityrds-xml-endpoint-notification-success-104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^\'<\/"]+)'] |