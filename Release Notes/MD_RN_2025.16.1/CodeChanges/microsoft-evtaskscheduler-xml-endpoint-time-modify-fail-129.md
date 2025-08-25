# Code Changes for microsoft-evtaskscheduler-xml-endpoint-time-modify-fail-129 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_id |  | ['<\/Data><Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<'] |
| edit_regex_field | dest_user_sid |  | ['<\/Data><Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<'] |