# Code Changes for hp-arubawc-kv-endpoint-login-success-connection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'auth_type', 'dest_ip', 'dest_port', 'host', 'session_id', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_ip |  | ['({auth_server}({host}[A-Fa-f:\d.]+))\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['({auth_server}({host}[A-Fa-f:\d.]+))\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | host |  | ['({auth_server}({host}[A-Fa-f:\d.]+))\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | time |  | ['({auth_server}({host}[A-Fa-f:\d.]+))\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | auth_server |  | ['({auth_server}({host}[A-Fa-f:\d.]+))\s({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| removed_attribute | DupFields |  | N/A |