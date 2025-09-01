# Code Changes for microsoft-evsecurity-xml-network-session-success-5158-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | layer_name |  | ['<Data Name\\*=(\'|")LayerName(\'|")>({layer_name}.+?)</Data>'] |
| edit_regex_field | ms_protocol_num |  | ['<Data Name\\*=(\'|")Protocol(\'|")>({ms_protocol_num}.+?)</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^"\\\/]+))</Data>'] |
| edit_regex_field | process_id |  | ['<Data Name\\*=(\'|")ProcessId(\'|")>({process_id}.+?)</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^"\\\/]+))</Data>'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")Application(\'|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^"\\\/]+))</Data>'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")SourceAddress(\'|")>(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)</Data>'] |
| edit_regex_field | src_port |  | ['<Data Name\\*=(\'|")SourceAddress(\'|")>(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)</Data>', '<Data Name\\*=(\'|")SourcePort(\'|")>({src_port}\d+)'] |