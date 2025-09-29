# Code Changes for crowdstrike-falcon-json-file-delete-success-deleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'aid', 'aip', 'email_address', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'hash_sha256', 'host', 'last_name', 'os', 'process_guid', 'src_file_dir', 'src_file_name', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | host |  | ['"ComputerName":"({host}[\w\-\.]+)"', 'exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)'] |
| added_regex_field | src_ip |  | ['"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |