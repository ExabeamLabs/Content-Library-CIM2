# Code Changes for trendmicro-ds-cef-app-activity-appactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_subject', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'domain', 'event_name', 'host', 'protocol', 'result', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_host |  | ['target=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+))'] |
| edit_regex_field | dest_ip |  | ['\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', 'target=(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+))'] |
| edit_regex_field | src_ip |  | ['\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['\Wspt=({src_port}\d+)', '\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| added_regex_field | alert_name |  | ['Alert:\s*({alert_name}[^=\\:]+)'] |
| added_regex_field | alert_severity |  | ['Severity:\s*({alert_severity}\S+)'] |
| added_regex_field | alert_subject |  | ['Subject:\s*({alert_subject}[^=\\:]+)'] |