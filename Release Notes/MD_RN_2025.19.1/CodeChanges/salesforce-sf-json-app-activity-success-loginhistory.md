# Code Changes for salesforce-sf-json-app-activity-success-loginhistory (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"EVENT_TYPE":"', '"ORGANIZATION_ID":"', '"REQUEST_ID":"', '"USER_ID":"'] |
| changed_parsed_fields | N/A |  | ['client_name', 'db_user', 'email_address', 'file_type', 'operation', 'src_ip', 'src_port', 'user_agent', 'user_type'] |
| edit_regex_field | operation |  | ['exa_json_path=$.DML_TYPE,exa_regex=(9999|({operation}[^"]+))$', 'exa_json_path=$.METHOD_NAME,exa_regex=(9999|({operation}[^"]+))$', 'exa_json_path=$.SHARING_OPERATION,exa_regex=(9999|({operation}[^"]+))$'] |
| edit_regex_field | src_ip |  | ['exa_json_path=$.CLIENT_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_json_path=$.SOURCE_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['exa_json_path=$.CLIENT_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_json_path=$.SOURCE_IP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | client_name |  | ['exa_json_path=$.CLIENT_NAME,exa_regex=(\\"\\"|({client_name}[^"]+))'] |
| added_regex_field | file_type |  | ['exa_json_path=$.FILE_TYPE,exa_regex=(UNKNOWN|({file_type}[^"]+))'] |
| added_regex_field | user_agent |  | ['exa_json_path=$.USER_AGENT,exa_regex=(9999|({user_agent}[^"]+))'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'app-login:fail', 'app-login:success', 'app-logout:success', 'http-request:fail', 'http-request:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'app-login', 'failed-app-login', 'web-activity-allowed', 'web-activity-denied'] |
| edit_attribute | Platform |  | ['Network', 'Salesforce'] |