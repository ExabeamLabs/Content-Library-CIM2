# Code Changes for vmware-esxi-kv-app-logout-success-loggedout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'browser', 'dest_host', 'domain', 'event_name', 'host', 'operation', 'os', 'time', 'user', 'user_agent'] |
| edit_regex_field | event_name |  | ['({operation}({event_name}logged out))'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({dest_host}({host}[\w\-\.]+))\s'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({dest_host}({host}[\w\-\.]+))\s'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({dest_host}({host}[\w\-\.]+))\s'] |
| added_regex_field | operation |  | ['({operation}({event_name}logged out))'] |
| removed_attribute | DupFields |  | N/A |