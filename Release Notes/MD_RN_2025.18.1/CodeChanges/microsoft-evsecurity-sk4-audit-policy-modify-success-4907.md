# Code Changes for microsoft-evsecurity-sk4-audit-policy-modify-success-4907 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['SubjectUserSid\':\s+(\'|")({user_sid}[^\'"]+)(\'|")'] |