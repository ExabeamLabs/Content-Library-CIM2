# Code Changes for crowdstrike-falcon-json-endpoint-logout-success-userlogoff (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'aip', 'auth_package', 'domain', 'email_address', 'event_name', 'host', 'linked_service_account', 'login_type', 'os', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'user_uid'] |
| added_regex_field | host |  | ['"ComputerName":"({host}[\w\-\.]+)"', 'exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)'] |
| added_regex_field | src_ip |  | ['"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | src_port |  | ['"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"', 'exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |