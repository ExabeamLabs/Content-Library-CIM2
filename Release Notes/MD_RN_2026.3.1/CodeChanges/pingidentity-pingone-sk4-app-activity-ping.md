# Code Changes for pingidentity-pingone-sk4-app-activity-ping (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['epoch', "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-dd-MM'T'HH:mm:ss.SSSZ"] |
| changed | Conditions |  | ['"source":', 'PingOne', 'destinationServiceName=Ping'] |
| changed_parsed_fields | N/A |  | ['additional_info', 'category', 'email_address', 'full_name', 'group_name', 'process_name', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | src_ip |  | ['exa_json_path=$.client.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['exa_json_path=$.client.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | email_address |  | ['exa_json_path=$..actors[?(@.type == \'user\')].name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))'] |
| added_regex_field | group_name |  | ['exa_json_path=$.actors[0].name,exa_regex=({group_name}[\s\w]+)@directory'] |
| added_attribute | ExtractionType |  | json |
| edit_attribute | activity_type |  | ['app-activity:success', 'app-login:fail', 'app-login:success', 'group-create:fail', 'group-create:success', 'group-delete:fail', 'group-delete:success', 'group-modify:fail', 'group-modify:success', 'policy-delete:fail', 'policy-delete:success', 'policy-modify:fail', 'policy-modify:success', 'user-create:fail', 'user-create:success', 'user-delete:fail', 'user-delete:success', 'user-disable:fail', 'user-disable:success', 'user-modify:fail', 'user-modify:success'] |
| edit_attribute | legacy_activity_type |  | ['account-creation', 'account-deleted', 'account-disabled', 'app-activity', 'app-activity-failed', 'app-login', 'failed-app-login'] |
| edit_attribute | Platform |  | ['Ping Identity', 'PingOne'] |