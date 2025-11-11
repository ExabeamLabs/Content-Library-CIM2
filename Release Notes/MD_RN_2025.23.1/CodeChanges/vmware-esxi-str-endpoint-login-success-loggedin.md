# Code Changes for vmware-esxi-str-endpoint-login-success-loggedin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_name', 'host', 'operation', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | host |  | ['(({dest_host}({host}[\w\-\.]+))\s+\d+)?\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '({dest_host}({host}[\w\-\.]+))\s*vpxd'] |
| edit_regex_field | time |  | ['(({dest_host}({host}[\w\-\.]+))\s+\d+)?\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |
| added_regex_field | dest_host |  | ['(({dest_host}({host}[\w\-\.]+))\s+\d+)?\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '({dest_host}({host}[\w\-\.]+))\s*vpxd'] |
| removed_attribute | DupFields |  | N/A |