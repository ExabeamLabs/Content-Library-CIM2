# Code Changes for microsoft-azuremon-json-app-activity-operationname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'db_user', 'resource_group', 'src_ip', 'src_port', 'subscription_id', 'user'] |
| edit_regex_field | src_ip |  | ['exa_json_path=$..EventIpAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$', 'exa_json_path=$..callerIpAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$', 'exa_json_path=$..ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$'] |
| edit_regex_field | src_port |  | ['exa_json_path=$..EventIpAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$', 'exa_json_path=$..callerIpAddress,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$', 'exa_json_path=$..ip,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$'] |
| edit_regex_field | user |  | ['exa_json_path=$..caller,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@([^"]+)', 'exa_json_path=$..user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | db_user |  | ['exa_regex="properties":\{[^\}]*?"category":"MySqlAuditLogs"[^\}]*?"user":"({db_user}[^"]+)"'] |
| added_attribute | event_timeFormat |  | ["yyyy-MM-dd'T'HH:mm:ssZ"] |