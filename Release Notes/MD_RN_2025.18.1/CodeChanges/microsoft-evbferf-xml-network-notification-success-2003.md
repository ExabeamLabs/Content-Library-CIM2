# Code Changes for microsoft-evbferf-xml-network-notification-success-2003 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | connection_id |  | ['<Data Name\\*=(\'|")ConnectionUsedId(\'|")>({connection_id}[^<]+)'] |
| edit_regex_field | dest_ip |  | ['<Data Name\\*=(\'|")RemoteIPAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['<Data Name\\*=(\'|")RemoteIPAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '<Data Name\\*=(\'|")RemotePort(\'|")>({dest_port}\d+)', '<Data Name\\*=(\'|")RemotePort(\'|")>({dest_port}\d+)'] |
| edit_regex_field | process_guid |  | ['<System>.*?Guid=(\'|")\{({process_guid}[^}]+)'] |
| edit_regex_field | protocol |  | ['<Data Name\\*=(\'|")Protocol(\'|")>({protocol}[^<]+)'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")LocalIPAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['<Data Name\\*=(\'|")LocalIPAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| changed | Conditions |  | ['<Data Name', '<EventID>2003</EventID>', 'ConnectionUsedId'] |