# Code Changes for microsoft-evazureadppdca-xml-user-password-reset-fail-30003 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | time |  | ['<TimeCreated SystemTime\\*=(\'|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,10}Z)(\'|")/>'] |
| edit_regex_field | user_sid |  | ['Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |