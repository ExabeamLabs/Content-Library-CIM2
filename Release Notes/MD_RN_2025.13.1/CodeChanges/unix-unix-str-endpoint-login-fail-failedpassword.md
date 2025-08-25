# Code Changes for unix-unix-str-endpoint-login-fail-failedpassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s+(::ffff:)?({host}[\w\-.]+)\s+', 'Message forwarded from ({host}[^\s:]+)'] |
| edit_regex_field | time |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s+(::ffff:)?({host}[\w\-.]+)\s+', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s+({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s'] |