# Code Changes for microsoft-evsecurity-mix-user-password-modify-4723 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user_sid |  | ['"TargetSid":"({dest_user_sid}S-[^\s"]+)"', '"TargetSid\\?"+:\\?"+({dest_user_sid}S-[^"\\]+)"', 'Target Account.+?Security ID:\s*(\\r|\\n|\\t)*({dest_user_sid}S-[^:\s]+?)(\\n|\\r|\\t)*\s*Account Name:'] |