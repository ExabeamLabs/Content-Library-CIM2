# Code Changes for vmware-esxi-str-endpoint-login-success-loggedin-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_host', 'domain', 'event_name', 'host', 'operation', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}logged in))'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({dest_host}({host}[\w\-\.]+))\s'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({dest_host}({host}[\w\-\.]+))\s'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({dest_host}({host}[\w\-\.]+))\s'] |
| added_regex_field | operation |  | ['({operation}({event_name}logged in))'] |
| removed_attribute | DupFields |  | N/A |