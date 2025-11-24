# Code Changes for manageengine-adssp-cef-app-activity-success-selfunlock (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'domain', 'email_address', 'event_name', 'host', 'object', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | email_address |  | ['LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({object}[\w\.\-\!\#\^\~]{1,40}\$?))', 'LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | object |  | ['LOGIN NAME\\?=(({email_address}[^@"]+@[^"\.]+.[^"]+)|({object}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |