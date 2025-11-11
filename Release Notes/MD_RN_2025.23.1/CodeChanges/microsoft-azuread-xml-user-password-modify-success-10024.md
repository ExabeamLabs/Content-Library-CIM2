# Code Changes for microsoft-azuread-xml-user-password-modify-success-10024 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_user', 'event_code', 'event_name', 'full_name', 'host', 'result', 'run_level', 'time', 'user', 'user_sid'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")Data1(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")Data1(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |