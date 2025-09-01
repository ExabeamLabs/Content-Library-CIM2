# Code Changes for microsoft-evsystem-xml-policy-apply-1500 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}.+?)(\'|")\/>'] |