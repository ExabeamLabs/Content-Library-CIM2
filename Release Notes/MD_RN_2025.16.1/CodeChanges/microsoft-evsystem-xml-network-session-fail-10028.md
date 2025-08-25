# Code Changes for microsoft-evsystem-xml-network-session-fail-10028 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_ip |  | ['<data name=(\'|")param1(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</data>'] |
| edit_regex_field | dest_port |  | ['<data name=(\'|")param1(\'|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?</data>'] |
| edit_regex_field | process_dir |  | ['<data name=(\'|")param3(\'|")>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))</data>'] |
| edit_regex_field | process_id |  | ['<execution processid=(\'|")({process_id}\d+)(\'|") threadid=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | process_name |  | ['<data name=(\'|")param3(\'|")>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))</data>'] |
| edit_regex_field | process_path |  | ['<data name=(\'|")param3(\'|")>({process_path}(({process_dir}[^<]*?)[\\\/]+)?({process_name}[^<\\\/]+))</data>'] |
| edit_regex_field | thread_id |  | ['<execution processid=(\'|")({process_id}\d+)(\'|") threadid=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | time |  | ['<TimeCreated SystemTime\\*=(\'|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '<timecreated systemtime=(\'|")({time}\d\d\d\d-\d\d-\d\dt\d\d:\d\d:\d\d\.\d{1,9}z)(\'|")/>'] |
| edit_regex_field | user_sid |  | ['<security userid=(\'|")({user_sid}[^\']+)(\'|")\/>'] |