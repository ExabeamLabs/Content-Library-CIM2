# Code Changes for microsoft-evsecurity-xml-network-session-fail-4984 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_ip |  | ['<Data Name\\*=(\'|")RemoteAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['<Data Name\\*=(\'|")RemoteAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '<Data Name\\*=(\'|")RemoteKeyModPort(\'|")>({dest_port}\d+)'] |
| edit_regex_field | failure_reason |  | ['<Data Name\\*=(\'|")FailureReason(\'|")>({failure_reason}[^<]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)'] |
| edit_regex_field | role |  | ['<Data Name\\*=(\'|")Role(\'|")>({role}[^<]+)'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")LocalAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['<Data Name\\*=(\'|")LocalAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '<Data Name\\*=(\'|")LocalKeyModPort(\'|")>({src_port}\d+)'] |
| edit_regex_field | state |  | ['<Data Name\\*=(\'|")State(\'|")>({state}[^<]+)'] |