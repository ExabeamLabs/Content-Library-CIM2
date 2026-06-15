# Code Changes for microsoft-evsecurity-xml-endpoint-time-modify-4616 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user_sid |  | ['<Security UserID(\\)?=(\'|")({user_sid}[^\'"]+)', 'Security ID:\s*({user_sid}\S+)\s+Account Name:', 'SubjectUserSid[^<>]+>({user_sid}[^<>]+)<'] |