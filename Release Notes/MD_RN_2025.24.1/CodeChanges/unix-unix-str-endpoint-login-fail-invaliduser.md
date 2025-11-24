# Code Changes for unix-unix-str-endpoint-login-fail-invaliduser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'email_address', 'event_code', 'failure_reason', 'host', 'login_id', 'process_id', 'process_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[-+]\d+:\d+)?\s*({dest_host}({host}[\w\-.]+))\s*sshd\[', '({time}\w+\s\d+\s\d+:\d+:\d+)(\s*({dest_host}({host}[\w\-.]+))(\s\w+)?\ssshd\[)?', '\d\d.*?\s({dest_host}({host}[\w\-\.]+))(:|\s|\s\w+)\s*sshd\[\d+\]'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[-+]\d+:\d+)?\s*({dest_host}({host}[\w\-.]+))\s*sshd\[', '({time}\w+\s\d+\s\d+:\d+:\d+)(\s*({dest_host}({host}[\w\-.]+))(\s\w+)?\ssshd\[)?'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[-+]\d+:\d+)?\s*({dest_host}({host}[\w\-.]+))\s*sshd\[', '({time}\w+\s\d+\s\d+:\d+:\d+)(\s*({dest_host}({host}[\w\-.]+))(\s\w+)?\ssshd\[)?', '\d\d.*?\s({dest_host}({host}[\w\-\.]+))(:|\s|\s\w+)\s*sshd\[\d+\]'] |
| removed_attribute | DupFields |  | N/A |