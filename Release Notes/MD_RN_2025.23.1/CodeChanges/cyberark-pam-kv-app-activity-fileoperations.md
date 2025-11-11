# Code Changes for cyberark-pam-kv-app-activity-fileoperations (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'account', 'additional_info', 'app', 'dest_host', 'dest_service_name', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'object', 'operation', 'safe_value', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ %CYBERARK', '({time}\w+ \d+ \d\d:\d\d:\d\d(Z)?)?\s*({dest_host}[\w\-.]+) %CYBERARK', '({time}\w+ \d+ \d\d:\d\d:\d\d(Z)?)?\s*({host}[\w\-.]+) %CYBERARK'] |
| added_regex_field | access |  | [';Message="({access}[^"]+)'] |
| added_regex_field | additional_info |  | [';File="({additional_info}[^"]+)'] |
| added_regex_field | dest_host |  | ['({time}\w+ \d+ \d\d:\d\d:\d\d(Z)?)?\s*({dest_host}[\w\-.]+) %CYBERARK'] |
| added_regex_field | object |  | [';File="[^"]*?[^"]+\\({object}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |