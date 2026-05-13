# Code Changes for unix-unix-str-endpoint-login-sshdconnectionfrom (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | [' Connection from ', ' sshd'] |
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'host', 'host_ip', 'process_id', 'process_name', 'src_ip', 'src_port', 'time'] |
| added_regex_field | dest_ip |  | ['\s+on\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+port\s*({dest_port}\d+)'] |
| added_regex_field | dest_port |  | ['\s+on\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+port\s*({dest_port}\d+)'] |