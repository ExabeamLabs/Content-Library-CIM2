# Code Changes for postgresql-p-str-database-login-fail-role-doesnt_exist (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | operation |  | ['(LOG|FATAL):\s*({operation}[^:]+)'] |
| edit_regex_field | src_ip |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?', 'client=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?'] |
| edit_regex_field | src_port |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?', 'client=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)'] |