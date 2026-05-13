# Code Changes for epic-siem-cef-app-activity-success-contextchange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_host', 'dest_ip', 'dest_port', 'host', 'object', 'operation', 'resource', 'result', 'role', 'src_host', 'user'] |
| removed_regex_field | additional_info |  | [] |
| edit_regex_field | resource |  | ['NEWDEPARTMENT=({resource}.+?)\s+(\w+=|$)', 'USERJOB=(|([^\^]+)?\^({resource}.+?))\s+(\w+=|$)'] |
| edit_regex_field | user |  | ['LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'PREVUSER=({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | dest_ip |  | ['IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | dest_port |  | ['IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | role |  | ['ROLE=({role}.+?)(\s+\w+=|\s*$)'] |