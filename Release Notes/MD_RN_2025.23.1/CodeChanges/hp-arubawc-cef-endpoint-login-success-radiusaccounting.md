# Code Changes for hp-arubawc-cef-endpoint-login-success-radiusaccounting (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_type', 'auth_server', 'dest_ip', 'dest_mac', 'dest_port', 'domain', 'email_address', 'host', 'network', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_port |  | ['\Wdst=({auth_server}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+([\w\.]+=|$)', '\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+([\w\.]+=|$)'] |
| added_regex_field | auth_server |  | ['\Wdst=({auth_server}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+([\w\.]+=|$)'] |
| removed_attribute | DupFields |  | N/A |