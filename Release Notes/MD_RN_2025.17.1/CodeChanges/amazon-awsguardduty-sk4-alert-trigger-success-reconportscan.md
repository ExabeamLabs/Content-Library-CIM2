# Code Changes for amazon-awsguardduty-sk4-alert-trigger-success-reconportscan (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_port |  | ['"resource":[^=]+?privateIpAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', '"service"[^\}]+"action"[^\}]+"portProbeAction"[^\}]+"portProbeDetails"[^\}]+"localPortDetails"[^\}]+"port":"?({dest_port}\d+)'] |