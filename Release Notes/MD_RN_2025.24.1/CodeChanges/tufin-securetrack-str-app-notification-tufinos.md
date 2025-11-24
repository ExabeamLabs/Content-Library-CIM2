# Code Changes for tufin-securetrack-str-app-notification-tufinos (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'host', 'src_host', 'src_ip', 'src_port'] |
| edit_regex_field | dest_host |  | ['TufinOS\(({host}({dest_host}[^\s:]+))\):\s+({src_host}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\(\d+\):*"*\s+({event_name}.+)\s'] |
| edit_regex_field | event_name |  | ['TufinOS\(({host}({dest_host}[^\s:]+))\):\s+({src_host}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\(\d+\):*"*\s+({event_name}.+)\s'] |
| edit_regex_field | src_host |  | ['TufinOS\(({host}({dest_host}[^\s:]+))\):\s+({src_host}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\(\d+\):*"*\s+({event_name}.+)\s'] |
| edit_regex_field | src_ip |  | ['TufinOS\(({host}({dest_host}[^\s:]+))\):\s+({src_host}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\(\d+\):*"*\s+({event_name}.+)\s'] |
| edit_regex_field | src_port |  | ['TufinOS\(({host}({dest_host}[^\s:]+))\):\s+({src_host}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\(\d+\):*"*\s+({event_name}.+)\s'] |
| added_regex_field | host |  | ['TufinOS\(({host}({dest_host}[^\s:]+))\):\s+({src_host}[^\s]+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\(\d+\):*"*\s+({event_name}.+)\s'] |
| removed_attribute | DupFields |  | N/A |