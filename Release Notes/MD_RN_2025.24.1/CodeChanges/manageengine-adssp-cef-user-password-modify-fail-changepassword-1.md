# Code Changes for manageengine-adssp-cef-user-password-modify-fail-changepassword-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_user', 'domain', 'email_address', 'event_name', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | email_address |  | ['LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_user |  | ['LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |