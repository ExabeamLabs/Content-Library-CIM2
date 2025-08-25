# Code Changes for s-xml-object-access (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_id |  | ['<\/Data><Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<'] |
| edit_regex_field | dest_user_sid |  | ['<\/Data><Data Name=(\'|")MemberSid(\'|")>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<'] |