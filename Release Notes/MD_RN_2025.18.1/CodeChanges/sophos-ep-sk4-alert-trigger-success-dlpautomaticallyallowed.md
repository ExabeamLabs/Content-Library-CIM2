# Code Changes for sophos-ep-sk4-alert-trigger-success-dlpautomaticallyallowed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['DATA_LOSS_PREVENTION', 'Event::Endpoint::DataLossPreventionAutomaticallyAllowed', 'endpoint_type'] |
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'bytes', 'device_type', 'domain', 'file_type', 'full_name', 'group_name', 'host', 'operation', 'result', 'rule', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'user', 'user_id'] |
| added_regex_field | device_type |  | ['"endpoint_type":"({device_type}[^"]+)'] |
| added_regex_field | full_name |  | ['"source":"(n\/a|(\d{1,3}\.){3}\d{1,3}|({full_name}[^"\\\(\)]+))","\w+'] |
| added_regex_field | group_name |  | ['"group":"({group_name}[^"]+)"'] |
| added_regex_field | src_ip |  | ['"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| added_regex_field | src_port |  | ['"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| added_regex_field | user_id |  | ['"user_id":"({user_id}[^"]+)'] |