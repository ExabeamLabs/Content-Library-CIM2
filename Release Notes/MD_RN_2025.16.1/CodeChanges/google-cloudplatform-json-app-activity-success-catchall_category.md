# Code Changes for google-cloudplatform-json-app-activity-success-catchall_category (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"] |
| changed_parsed_fields | N/A |  | ['email_address', 'resource_dir', 'resource_name', 'resource_path', 'src_ip', 'src_port'] |
| edit_regex_field | email_address |  | ['exa_json_path=$..username,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)'] |
| edit_regex_field | src_ip |  | ['exa_json_path=$..remote_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['exa_json_path=$..remote_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | resource_dir |  | ['exa_json_path=$..resourceName,exa_regex=({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))'] |
| added_regex_field | resource_name |  | ['exa_json_path=$..resourceName,exa_regex=({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))'] |
| added_regex_field | resource_path |  | ['exa_json_path=$..resourceName,exa_regex=({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))'] |