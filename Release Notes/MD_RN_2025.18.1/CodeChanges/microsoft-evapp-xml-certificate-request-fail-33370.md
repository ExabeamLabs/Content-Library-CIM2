# Code Changes for microsoft-evapp-xml-certificate-request-fail-33370 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | failure_reason |  | ['<Data Name\\*=(\'|")ErrorCode(\'|")>({failure_reason}[^<]+?)</Data>', '<Data Name\\*=(\'|")ErrorDescription(\'|")>({failure_reason}[^<]+?)\s*</Data>'] |
| edit_regex_field | user_id |  | ['<Security UserID\\*=(\'|")(({user_sid}S-[^\\'"]+)|({user_id}[^\\'"]+))'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")(({user_sid}S-[^\\'"]+)|({user_id}[^\\'"]+))', 'Security ID:\s*({user_sid}\S+)\s+Account Name:'] |