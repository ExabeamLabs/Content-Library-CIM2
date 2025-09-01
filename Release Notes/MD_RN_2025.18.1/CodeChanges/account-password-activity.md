# Code Changes for account-password-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |