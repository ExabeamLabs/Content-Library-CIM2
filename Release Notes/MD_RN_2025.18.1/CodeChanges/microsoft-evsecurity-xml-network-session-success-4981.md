# Code Changes for microsoft-evsecurity-xml-network-session-success-4981 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['<Data Name\\*=(\'|")RemoteMMPrincipalName(\'|")>({dest_host}[\w\-.]+)'] |
| edit_regex_field | dest_ip |  | ['<Data Name\\*=(\'|")RemoteAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['<Data Name\\*=(\'|")RemoteAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '<Data Name\\*=(\'|")RemoteKeyModPort(\'|")>({dest_port}\d+)'] |
| edit_regex_field | duration |  | ['<Data Name\\*=(\'|")MMLifetime(\'|")>({duration}[^<]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | src_host |  | ['<Data Name\\*=(\'|")LocalMMPrincipalName(\'|")>({src_host}[^<]+)'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")LocalAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['<Data Name\\*=(\'|")LocalAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '<Data Name\\*=(\'|")LocalKeyModPort(\'|")>({src_port}\d+)'] |