# Code Changes for juniper-ps-kv-vpn-login-success-sso (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+))\s+(Juniper|PulseSecure):', 'PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | host |  | ['PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | time |  | ['PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |