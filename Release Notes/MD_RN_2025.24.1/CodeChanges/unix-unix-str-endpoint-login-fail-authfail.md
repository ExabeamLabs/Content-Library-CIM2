# Code Changes for unix-unix-str-endpoint-login-fail-authfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'failure_reason', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d \d\d\d\d ({dest_host}({host}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |