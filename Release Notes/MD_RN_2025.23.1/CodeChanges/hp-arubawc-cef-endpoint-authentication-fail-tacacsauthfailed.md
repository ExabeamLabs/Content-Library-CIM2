# Code Changes for hp-arubawc-cef-endpoint-authentication-fail-tacacsauthfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'auth_server', 'dest_ip', 'dest_mac', 'dest_port', 'failure_reason', 'host', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_port |  | ['cs1=({auth_server}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\w+=', 'cs1=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\w+='] |
| added_regex_field | auth_server |  | ['cs1=({auth_server}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s\w+='] |
| removed_attribute | DupFields |  | N/A |