# Code Changes for microsoft-evsystem-xml-network-session-fail-10028-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['<Computer>', "<EventID Qualifiers='", '<Provider Name=', '>10028<', 'Microsoft-Windows-DistributedCOM'] |
| edit_regex_field | dest_host |  | ['<Data Name=(\'|")param1(\'|")>(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))</Data>'] |
| edit_regex_field | dest_ip |  | ['<Data Name=(\'|")param1(\'|")>(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))</Data>'] |
| edit_regex_field | dest_port |  | ['<Data Name=(\'|")param1(\'|")>(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name=(\'|")param3(\'|")>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))<\/Data>'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | process_name |  | ['<Data Name=(\'|")param3(\'|")>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name=(\'|")param3(\'|")>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))<\/Data>'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID=(\'|")({process_id}\d+)(\'|") ThreadID=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[^\'"]+)(\'|")\/>'] |