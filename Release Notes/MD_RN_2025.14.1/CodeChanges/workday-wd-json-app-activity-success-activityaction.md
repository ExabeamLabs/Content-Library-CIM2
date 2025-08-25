# Code Changes for workday-wd-json-app-activity-success-activityaction (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed | Conditions | ['"activityAction":', '"tenantHost":', 'workday'] | ['"activityAction":', '"systemAccount":', '"taskDisplayName":'] |
| changed_parsed_fields | N/A | ['app', 'src_ip', 'src_port', 'user'] | ['additional_info', 'app', 'device_type', 'operation', 'session_id', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | app | ['exa_regex=({app}(W|w)orkday)'] | ['({app}(W|w)orkday)', 'exa_regex=({app}(W|w)orkday)'] |
| edit_regex_field | src_ip | ['exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] | ['"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port | ['exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] | ['"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?', 'exa_json_path=$.ipAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | user | ['exa_json_path=$.systemAccount,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$'] | ['"systemAccount":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'exa_json_path=$.systemAccount,exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$'] |
| added_regex_field | additional_info | [] | ['"activityAction":"({additional_info}[^"]+)'] |
| added_regex_field | device_type | [] | ['"deviceType":"({device_type}[^"]+)'] |
| added_regex_field | operation | [] | ['"taskDisplayName":"({operation}[^"]+)'] |
| added_regex_field | session_id | [] | ['"sessionId":"({session_id}[^"]+)'] |
| added_regex_field | time | [] | ['"requestTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)'] |
| added_regex_field | user_agent | [] | ['"userAgent":"({user_agent}[^"]+)'] |