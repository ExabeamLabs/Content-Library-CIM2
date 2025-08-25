# Code Changes for microsoft-evsecurity-xml-network-session-success-5158 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_ip |  | ['<Data Name\\*=(\'|")DestAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</Data>'] |
| edit_regex_field | dest_port |  | ['<Data Name\\*=(\'|")DestAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</Data>', '<Data Name\\*=(\'|")DestPort(\'|")>({dest_port}\d+)</Data>'] |
| edit_regex_field | layer_name |  | ['<Data Name\\*=(\'|")LayerName(\'|")>\s*({layer_name}[^<]+?)\s*</Data>'] |
| edit_regex_field | ms_protocol_num |  | ['<Data Name\\*=(\'|")Protocol(\'|")>({ms_protocol_num}\d+)</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))</Data>'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}[^<>]+)</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}(?:[^<]+)?[\\\/])?({process_name}[^\\\/]+?))</Data>'] |
| edit_regex_field | protocol |  | ['<Data Name\\*=(\'|")Protocol(\'|")>({protocol}[^<]+)<'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")SourceAddress(\'|")>(::|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)</Data>'] |
| edit_regex_field | src_port |  | ['<Data Name\\*=(\'|")SourceAddress(\'|")>(::|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)</Data>', '<Data Name\\*=(\'|")SourcePort(\'|")>({src_port}\d+)</Data>'] |
| edit_regex_field | time |  | ['<TimeCreated SystemTime\\*=(\'|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)\d+Z(\'|")/>'] |