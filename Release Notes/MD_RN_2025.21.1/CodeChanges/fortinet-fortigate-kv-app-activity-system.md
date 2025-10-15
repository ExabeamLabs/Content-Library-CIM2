# Code Changes for fortinet-fortigate-kv-app-activity-system (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'community', 'dest_ip', 'dest_port', 'devid', 'domain', 'email_address', 'event_name', 'host', 'method', 'operation', 'result', 'result_reason', 'severity', 'src_ip', 'src_port', 'time', 'user', 'version'] |
| removed_regex_field | alert_name |  | [] |
| removed_regex_field | alert_severity |  | [] |
| added_regex_field | action |  | ['\saction="({action}[^"]+)"'] |
| added_regex_field | dest_ip |  | ['\sdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | dest_port |  | ['\sdstip="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | event_name |  | ['\slogdesc="({event_name}[^"]+?)"'] |
| added_regex_field | method |  | ['\smethod="(none|({method}[^"]+))"'] |
| added_regex_field | result |  | ['\sstatus="({result}[^"]+)"'] |
| added_regex_field | result_reason |  | ['\sreason="(none|({result_reason}[^"]+))"'] |
| added_regex_field | severity |  | ['\slevel="({severity}[^"]+?)"'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'app-login:fail', 'app-login:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'app-login', 'failed-app-login'] |