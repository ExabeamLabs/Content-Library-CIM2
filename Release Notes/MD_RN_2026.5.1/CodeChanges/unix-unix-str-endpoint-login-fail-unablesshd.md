# Code Changes for unix-unix-str-endpoint-login-fail-unablesshd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", 'MMM dd HH:mm:ss', 'MMM dd HH:mm:ss yyyy', 'MMM d HH:mm:ss yyyy', 'MMM  d HH:mm:ss yyyy', 'yyyy-MM-dd HH:mm:ss'] |
| changed | Conditions |  | [' Unable to negotiate ', ' sshd'] |
| changed_parsed_fields | N/A |  | ['dest_host', 'dest_ip', 'failure_reason', 'host', 'host_ip', 'process_id', 'process_name', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_host |  | ['\w+\s+\d+\s+\d+:\d+:\d+\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))\s+sshd'] |
| edit_regex_field | dest_ip |  | ['\w+\s+\d+\s+\d+:\d+:\d+\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))\s+sshd'] |
| edit_regex_field | host |  | ['(\w+\s+\d+\s\d\d:\d\d:\d\d)?\s*(::ffff:)?({host}[\w.-]+)? sshd\[', '({time}\w+\s+\d+\s+\d\d:\d\d:\d\d \d\d\d\d)\s(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))(\sAP:({=host}[\w.-]+)\s+\<[^>]+\>)?\ssshd\[', '\w+\s+\d+\s+\d+:\d+:\d+\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))\s+sshd'] |
| added_regex_field | host_ip |  | ['({time}\w+\s+\d+\s+\d\d:\d\d:\d\d \d\d\d\d)\s(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))(\sAP:({=host}[\w.-]+)\s+\<[^>]+\>)?\ssshd\['] |
| added_regex_field | time |  | ['({time}\w+\s+\d+\s+\d\d:\d\d:\d\d \d\d\d\d)\s(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({host}[\w\-\.]+))(\sAP:({=host}[\w.-]+)\s+\<[^>]+\>)?\ssshd\['] |