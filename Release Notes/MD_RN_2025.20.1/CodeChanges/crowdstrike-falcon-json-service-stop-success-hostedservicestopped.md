# Code Changes for crowdstrike-falcon-json-service-stop-success-hostedservicestopped (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'aip', 'app', 'cid', 'dest_process_id', 'dproc', 'event_name', 'host', 'os', 'service_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | src_ip |  | ['"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', '"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| added_regex_field | aip |  | ['"aip":\s*"({aip}[^"]+)"'] |
| added_regex_field | host |  | ['"ComputerName":"({host}[\w\-\.]+)"', 'exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)'] |
| added_regex_field | src_port |  | ['"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |