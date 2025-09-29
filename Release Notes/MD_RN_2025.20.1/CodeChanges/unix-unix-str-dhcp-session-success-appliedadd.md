# Code Changes for unix-unix-str-dhcp-session-success-appliedadd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'host'] |
| edit_regex_field | dest_host |  | ["applied ADD for '(((\w+-)?({dest_mac}([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})))|({dest_host}[^']+))'.+? IN A ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"] |
| edit_regex_field | dest_ip |  | ["applied ADD for '(((\w+-)?({dest_mac}([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})))|({dest_host}[^']+))'.+? IN A ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"] |
| edit_regex_field | dest_port |  | ["applied ADD for '(((\w+-)?({dest_mac}([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})))|({dest_host}[^']+))'.+? IN A ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"] |
| added_regex_field | dest_mac |  | ["applied ADD for '(((\w+-)?({dest_mac}([0-9A-Fa-f]{2}[:-]){5}([0-9A-Fa-f]{2})))|({dest_host}[^']+))'.+? IN A ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"] |