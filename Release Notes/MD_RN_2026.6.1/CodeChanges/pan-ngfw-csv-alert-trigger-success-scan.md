# Code Changes for pan-ngfw-csv-alert-trigger-success-scan (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_ip |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,THREAT,({alert_type}[^,]+),([^,]*,){2}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),', ',THREAT,([^,]*,){4}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | dest_port |  | [',THREAT,([^,]*,){21}(0|({dest_port}\d+)),', ',THREAT,([^,]*,){4}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| edit_regex_field | src_ip |  | ['({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,THREAT,({alert_type}[^,]+),([^,]*,){2}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),', ',THREAT,([^,]*,){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | [',THREAT,([^,]*,){20}(0|({src_port}\d+)),', ',THREAT,([^,]*,){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |