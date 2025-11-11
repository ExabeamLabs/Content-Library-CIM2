# Code Changes for crowdstrike-falcon-cef-file-write-success-critialfilemodified (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'aip', 'cid', 'dest_host', 'dest_ip', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'os', 'src_port', 'time', 'user'] |
| removed_regex_field | src_ip |  | [] |
| edit_regex_field | src_port |  | ['"LocalAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', '"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | dest_host |  | ['"ComputerName":"({dest_host}[\w\-\.]+)"', 'exa_json_path=$.ComputerName,exa_regex=({dest_host}[\w\-\.]+)'] |
| added_regex_field | dest_ip |  | ['"LocalAddressIP4":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | user |  | ['exa_json_path=$.UserName,exa_regex=({user}[\w\.\-]{1,40}\$?)', 'suser=({user}[\w\.\-]{1,40}\$?)\s\w+='] |
| edit_attribute | Platform |  | ['Falcon', 'MacOS', 'Unix', 'Windows'] |