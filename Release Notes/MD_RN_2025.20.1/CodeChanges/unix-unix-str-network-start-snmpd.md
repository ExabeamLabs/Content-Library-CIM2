# Code Changes for unix-unix-str-network-start-snmpd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'event_name', 'host', 'process_id', 'process_name', 'protocol', 'src_ip', 'src_port'] |
| edit_regex_field | process_id |  | ['\d\d:\d\d:\d\d ({host}[\w\-.]+)(\s\w+)?\s({event_name}[^\[]+)\s*\[({process_id}[^\]]+)\]:\s*Connection from ({protocol}[^\:\s]+):\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]:({src_port}\d+)->\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| added_regex_field | process_name |  | ['\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |