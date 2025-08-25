# Code Changes for microsoft-evsecurity-xml-endpoint-authentication-success-3000 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_guid |  | ['Guid=(\'|")\{({process_guid}[^\}\'"]+?)\}(\'|")'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | provider_name |  | ['<Provider Name=(\'|")({provider_name}[^\'"]+)(\'|")'] |
| edit_regex_field | src_host |  | ['<Data Name=(\'|")ClientName(\'|")>((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)|({src_host}[\w.-]+))<'] |
| edit_regex_field | src_ip |  | ['<Data Name=(\'|")ClientName(\'|")>((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)|({src_host}[\w.-]+))<'] |
| edit_regex_field | src_port |  | ['<Data Name=(\'|")ClientName(\'|")>((({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)|({src_host}[\w.-]+))<'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[^\'"]+)(\'|")\/>'] |