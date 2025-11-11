# Code Changes for cyberark-vault-kv-user-password-modify-fail-changepassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | [';Address="(|(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\:({dest_port}\d+))?|({dest_host}[\w\-.]+)))"', '\d\d:\d\d:\d\d(Z)? ({dest_host}({host}[\w\-.]+)) %CYBERARK'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(Z)? ({dest_host}({host}[\w\-.]+)) %CYBERARK'] |
| removed_attribute | DupFields |  | N/A |