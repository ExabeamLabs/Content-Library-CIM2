# Code Changes for postgresql-p-str-database-activity-fail-error (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['ERROR:', 'db=', 'pid='] |
| edit_regex_field | db_name |  | ['\):({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({db_name}[^:]+):\[', 'db=({db_name}[^,]+)'] |
| edit_regex_field | operation |  | ['({operation_type}ERROR):\s*({operation}[^:"]+)', ':({operation_type}ERROR):\s*({operation}[^:"]+)'] |
| edit_regex_field | operation_type |  | ['({operation_type}ERROR):\s*({operation}[^:"]+)', ':({operation_type}ERROR):\s*({operation}[^:"]+)'] |
| edit_regex_field | src_ip |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?', 'client=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?'] |
| edit_regex_field | src_port |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?', 'client=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)'] |
| edit_regex_field | user |  | ['\):({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({db_name}[^:]+):\[', 'user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |