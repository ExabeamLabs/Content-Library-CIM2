# Code Changes for google-gcpca-sk4-app-activity-cloud (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_severity', 'app', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'http_response_code', 'log_name', 'method', 'operation', 'permission', 'project_id', 'region', 'resource_path', 'resource_type', 'result', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_agent'] |
| edit_regex_field | result |  | ['"granted":({result}[^,":\}]+)', '"outcome":"({result}[^"]+)'] |
| edit_regex_field | src_ip |  | ['"callerIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '"remoteIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['"callerIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', '"remoteIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | user_agent |  | ['"callerSuppliedUserAgent":"({user_agent}[^"]+)', '"userAgent":"({user_agent}[^"]+)"'] |
| added_regex_field | additional_info |  | ['latency":\{({additional_info}[^\}]+)'] |
| added_regex_field | dest_ip |  | ['"serverIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"'] |
| added_regex_field | dest_port |  | ['"serverIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"'] |
| added_regex_field | http_response_code |  | ['"status":({http_response_code}\d+)'] |
| added_regex_field | log_name |  | ['log-name":"({log_name}[^"]+)'] |
| added_regex_field | method |  | ['requestMethod":\{"constant":"({method}[^"\}]+)"\}'] |
| added_regex_field | project_id |  | ['"project_id":"({project_id}[^"]+)"'] |
| added_regex_field | url |  | ['"requestUrl":"({url}[^"]+)"'] |