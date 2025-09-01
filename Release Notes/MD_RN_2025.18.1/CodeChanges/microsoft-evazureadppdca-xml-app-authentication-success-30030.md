# Code Changes for microsoft-evazureadppdca-xml-app-authentication-success-30030 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |