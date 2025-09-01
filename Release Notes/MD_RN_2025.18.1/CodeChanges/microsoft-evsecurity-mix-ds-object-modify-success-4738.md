# Code Changes for microsoft-evsecurity-mix-ds-object-modify-success-4738 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>({dest_user_sid}[^<]+)', 'Target\sAccount[\s\S]*?Security ID:\s*({dest_user_sid}[^:]+?)\s'] |
| edit_regex_field | new_attribute |  | ['<Data Name\\*=(\'|")NewUacValue(\'|")>({new_attribute}[^<]+)'] |
| edit_regex_field | old_attribute |  | ['<Data Name\\*=(\'|")OldUacValue(\'|")>({old_attribute}[^<]+)'] |