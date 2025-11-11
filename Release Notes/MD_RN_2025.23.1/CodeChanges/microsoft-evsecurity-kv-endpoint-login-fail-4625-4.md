# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4625-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'login_type', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['(\s({dest_host}({host}[^\s]+))\s)?({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))'] |
| edit_regex_field | src_host_windows |  | ['Nombre de estación de trabajo:\s*({src_host_windows}({src_host}[\w\-\.]+))\s*Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*Puerto de orig'] |
| edit_regex_field | src_ip |  | ['Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'Nombre de estación de trabajo:\s*({src_host_windows}({src_host}[\w\-\.]+))\s*Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*Puerto de orig'] |
| edit_regex_field | src_port |  | ['Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'Nombre de estación de trabajo:\s*({src_host_windows}({src_host}[\w\-\.]+))\s*Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*Puerto de orig'] |
| edit_regex_field | time |  | ['(\s({dest_host}({host}[^\s]+))\s)?({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))'] |
| added_regex_field | dest_host |  | ['(\s({dest_host}({host}[^\s]+))\s)?({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))'] |
| added_regex_field | src_host |  | ['Nombre de estación de trabajo:\s*({src_host_windows}({src_host}[\w\-\.]+))\s*Dirección de red de origen:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*Puerto de orig'] |
| removed_attribute | DupFields |  | N/A |