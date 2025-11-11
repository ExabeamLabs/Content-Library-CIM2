# Code Changes for fireeye-networksecurity-json-alert-trigger-success-alert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['yyyy-MM-dd HH:mm:ss', "yyyy-MM-dd'T'HH:mm:ssZ"] |
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_mac', 'dest_port', 'event_url', 'host', 'proxy_ip', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time'] |
| edit_regex_field | alert_name |  | ['"explanation":\s\{\s*(?:"\w+": "[^"]+",\s*)*"({alert_type}[^"]+)": \{\s*[^\{]+\{\s*(?:"\w+": "[^"]+",\s*)*"name": "({alert_name}[^"]+)"', '"malware":\s*\{[^\}]+?"name":\s*"({alert_name}[^"]+)"'] |
| edit_regex_field | src_port |  | ['"src":\s*\{[^\}]+?"port":\s*"({src_port}\d+)"', '"src":\s\{\s*(?:"\w+": "[^"]+",\s*)*"ip": "({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"'] |
| edit_regex_field | time |  | ['"occurred": "({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})', '"occurred":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"'] |
| added_regex_field | dest_ip |  | ['"dst":\s*\{\s*"ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"'] |
| added_regex_field | dest_mac |  | ['"dst":\s*\{[^\}]+?"mac":\s*"({dest_mac}[^"]+)"'] |
| added_regex_field | dest_port |  | ['"dst":\s*\{[^\}]+?"port":\s*"({dest_port}\d+)"'] |
| added_regex_field | event_url |  | ['"alert":\s\{[^\}]+?"alert-url":\s*"({event_url}[^"]+)"'] |
| added_regex_field | proxy_ip |  | ['"proxy":\s*"({proxy_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))'] |
| added_regex_field | src_mac |  | ['"src":\s*\{[^\}]+?"mac":\s*"({src_mac}[^"]+)"'] |
| removed_attribute | SOAR |  | N/A |