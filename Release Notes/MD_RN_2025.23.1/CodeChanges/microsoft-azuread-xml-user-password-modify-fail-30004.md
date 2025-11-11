# Code Changes for microsoft-azuread-xml-user-password-modify-fail-30004 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'event_code', 'event_name', 'full_name', 'host', 'result', 'run_level', 'time', 'user', 'user_sid'] |
| edit_regex_field | user |  | ['UserName:\s*({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_user |  | ['UserName:\s*({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |