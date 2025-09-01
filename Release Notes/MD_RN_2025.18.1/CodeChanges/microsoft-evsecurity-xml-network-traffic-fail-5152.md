# Code Changes for microsoft-evsecurity-xml-network-traffic-fail-5152 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_ip |  | ['<Data Name(\\)?=(\'|")DestAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | ['<Data Name(\\)?=(\'|")DestAddress(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '<Data Name(\\)?=(\'|")DestPort(\'|")>({dest_port}\d+)'] |
| edit_regex_field | direction |  | ['<Data Name\\*=(\'|")Direction(\'|")>({direction}(Inbound|Outbound))</Data>', 'Direction:((?-i)\\+[rnt])*\s*({direction}Outbound|Inbound)', 'Direction:[\s\S]*?({direction}[^\s]+)'] |
| edit_regex_field | process_dir |  | ['<Data Name(\\)?=(\'|")Application(\'|")>(-|({process_path}({process_dir}([^<]+)?[\\\/])?({process_name}[^\\\/]+?)))<'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID(\\)?=(\'|")({process_id}\d+)'] |
| edit_regex_field | process_name |  | ['<Data Name(\\)?=(\'|")Application(\'|")>(-|({process_path}({process_dir}([^<]+)?[\\\/])?({process_name}[^\\\/]+?)))<'] |
| edit_regex_field | process_path |  | ['<Data Name(\\)?=(\'|")Application(\'|")>(-|({process_path}({process_dir}([^<]+)?[\\\/])?({process_name}[^\\\/]+?)))<'] |
| edit_regex_field | protocol |  | ['<Data Name(\\)?=(\'|")Protocol(\'|")>({protocol}[^<]+)'] |
| edit_regex_field | src_ip |  | ['<Data Name(\\)?=(\'|")SourceAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['<Data Name(\\)?=(\'|")SourceAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '<Data Name(\\)?=(\'|")SourcePort(\'|")>({src_port}\d+)'] |