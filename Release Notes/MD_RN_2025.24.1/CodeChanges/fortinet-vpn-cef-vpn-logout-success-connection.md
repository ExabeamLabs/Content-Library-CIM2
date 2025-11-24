# Code Changes for fortinet-vpn-cef-vpn-logout-success-connection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes_in', 'bytes_out', 'dest_ip', 'dest_port', 'email_address', 'host', 'src_ip', 'src_port', 'time', 'tz', 'user'] |
| added_regex_field | dest_ip |  | ['\sloc_?ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | dest_port |  | ['\sloc_?ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |