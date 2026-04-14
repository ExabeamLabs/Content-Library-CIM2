# Code Changes for jumpcloud-jc-json-directoryinsights-events (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['country_code', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'host', 'mfa', 'os', 'os_version', 'process_dir', 'process_name', 'process_path', 'region', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['exa_json_path=$.system.hostname,exa_regex=({host}[\w\-\.]+)', 'exa_json_path=$.system.hostname,exa_regex=({host}[\w\-\.]+)'] |
| edit_regex_field | src_ip |  | ['"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_json_path=$.client_ip,exa_regex=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(::ffff:)?({=src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?)', 'exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['"client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_json_path=$.client_ip,exa_regex=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|(::ffff:)?({=src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?)', 'exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | user |  | ['"username":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', 'exa_json_path=$.initiated_by.username,exa_regex=({user}[\w\.\-]{1,40}\$?)', 'exa_json_path=$.initiated_by.username,exa_regex=({user}[\w\.\-]{1,40}\$?)', 'exa_json_path=$.resource.username,exa_regex=({user}[\w\.\-]{1,40}\$?)', 'exa_json_path=$.username,exa_regex=({user}[\w\.\-]{1,40}\$?)'] |
| added_regex_field | country_code |  | ['"country_code":"({country_code}[^"]+)"'] |
| added_regex_field | event_name |  | ['"event_type":"({event_name}[^"]+)"'] |
| added_regex_field | failure_reason |  | ['error_message":"({failure_reason}[^",]+)"'] |
| added_regex_field | mfa |  | ['"mfa":({mfa}[^",]+)'] |
| added_regex_field | os |  | ['"os_name":"({os}[^"]+)"'] |
| added_regex_field | os_version |  | ['"os_version":"({os_version}[^"]+)"'] |
| added_regex_field | process_dir |  | ['exa_json_path=$.process_name,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))'] |
| added_regex_field | process_name |  | ['exa_json_path=$.process_name,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))'] |
| added_regex_field | process_path |  | ['exa_json_path=$.process_name,exa_regex=({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))'] |
| added_regex_field | region |  | ['"region_name":"({region}[^"]+)"'] |
| added_regex_field | time |  | ['"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)'] |