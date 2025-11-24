# Code Changes for unix-unix-str-endpoint-login-fail-manyauthfail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'event_name', 'failure_reason', 'host', 'process_id', 'process_name', 'src_ip', 'user'] |
| edit_regex_field | event_name |  | ['({failure_reason}({event_name}Too many authentication failures)) for ({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w.\-]+))\s+sshd\['] |
| edit_regex_field | user |  | ['({failure_reason}({event_name}Too many authentication failures)) for ({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w.\-]+))\s+sshd\['] |
| added_regex_field | failure_reason |  | ['({failure_reason}({event_name}Too many authentication failures)) for ({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| removed_attribute | DupFields |  | N/A |