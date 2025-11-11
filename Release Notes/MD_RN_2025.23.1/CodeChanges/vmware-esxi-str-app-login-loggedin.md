# Code Changes for vmware-esxi-str-app-login-loggedin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_name', 'host', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({dest_host}({host}[\w\-\.]+))\sHostd:'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({dest_host}({host}[\w\-\.]+))\sHostd:'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({dest_host}({host}[\w\-\.]+))\sHostd:'] |
| removed_attribute | DupFields |  | N/A |