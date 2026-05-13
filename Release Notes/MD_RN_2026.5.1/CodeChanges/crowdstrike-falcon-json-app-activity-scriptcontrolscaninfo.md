# Code Changes for crowdstrike-falcon-json-app-activity-scriptcontrolscaninfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'aip', 'cid', 'event_code', 'event_name', 'old_hash', 'operation', 'os', 'process_id', 'src_ip', 'src_port', 'time', 'web_content_type'] |
| edit_regex_field | event_code |  | ['"event_simpleName":\s*"({operation}({event_code}[^"]+))"'] |
| edit_regex_field | os |  | ['"event_platform":"({os}[^"]+)"', '({os}Linux)', 'exa_regex=({os}Linux)'] |
| edit_regex_field | src_port |  | ['"LocalAddressIP4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.aip,exa_regex=({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_regex="LocalAddressIP4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| added_regex_field | operation |  | ['"event_simpleName":\s*"({operation}({event_code}[^"]+))"'] |
| added_regex_field | src_ip |  | ['"LocalAddressIP4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_regex="LocalAddressIP4":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |