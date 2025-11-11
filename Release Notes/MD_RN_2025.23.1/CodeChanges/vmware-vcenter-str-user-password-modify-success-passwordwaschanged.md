# Code Changes for vmware-vcenter-str-user-password-modify-success-passwordwaschanged (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'result', 'service_name', 'src_host', 'time', 'user'] |
| edit_regex_field | event_name |  | ['\s({result}({event_name}Password was changed)) for account ({user}[\w\.\-\!\#\^\~]{1,40}\$?)', '\s({user}[\w\.\-\!\#\^\~]{1,40}\$?) account ({result}({event_name}password was changed))'] |
| edit_regex_field | user |  | ['\s({result}({event_name}Password was changed)) for account ({user}[\w\.\-\!\#\^\~]{1,40}\$?)', '\s({user}[\w\.\-\!\#\^\~]{1,40}\$?) account ({result}({event_name}password was changed))'] |
| added_regex_field | result |  | ['\s({result}({event_name}Password was changed)) for account ({user}[\w\.\-\!\#\^\~]{1,40}\$?)', '\s({user}[\w\.\-\!\#\^\~]{1,40}\$?) account ({result}({event_name}password was changed))'] |
| removed_attribute | DupFields |  | N/A |