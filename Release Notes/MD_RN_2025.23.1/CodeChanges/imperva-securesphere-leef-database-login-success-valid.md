# Code Changes for imperva-securesphere-leef-database-login-success-valid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'db_name', 'dest_ip', 'dest_port', 'domain', 'host', 'result', 'result_reason', 'server_group', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | src_ip |  | ['src=((?=0\.0\.0\.0)|({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?)'] |
| edit_regex_field | src_port |  | ['src=((?=0\.0\.0\.0)|({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?)'] |
| added_regex_field | host |  | ['src=((?=0\.0\.0\.0)|({host}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?)'] |
| removed_attribute | DupFields |  | N/A |