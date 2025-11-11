# Code Changes for cyberark-pam-kv-user-password-modify-success-cpmpasswordchanged (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['({time}\w+ \d+ \d\d:\d\d:\d\d(Z)?)?\s*({dest_host}[\w\-.]+) %CYBERARK', ';Address="(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+)))"'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ) \S+ %CYBERARK', '({time}\w+ \d+ \d\d:\d\d:\d\d(Z)?)?\s*({dest_host}[\w\-.]+) %CYBERARK', '({time}\w+ \d+ \d\d:\d\d:\d\d(Z)?)?\s*({host}[\w\-.]+) %CYBERARK'] |
| removed_attribute | DupFields |  | N/A |