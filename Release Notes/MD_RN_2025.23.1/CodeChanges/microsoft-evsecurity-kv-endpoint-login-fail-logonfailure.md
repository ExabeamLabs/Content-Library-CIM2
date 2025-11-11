# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-logonfailure (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_package', 'auth_process', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type', 'result_code', 'src_domain', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| edit_regex_field | event_code |  | ['({host}[^\s\/]+)\/Security \(({result_code}({event_code}\d+))\)', 'Event(ID)?Code=({result_code}({event_code}\d+))', '\d\d:\d\d:\d\d \d\d\d\d\s*(\s|\t|,|#\d+|<[^>]+>)\s*({result_code}({event_code}\d+))\s*(\s|\t|,|#\d+|<[^>]+>)\s*Security'] |
| edit_regex_field | host |  | ['(?i)(((audit|failure)( |_)(audit|failure))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*', '({host}[^\s\/]+)\/Security \(({result_code}({event_code}\d+))\)', '<Computer>({dest_host}({host}[\w\-.]+))</Computer>', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)', 'Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s)'] |
| added_regex_field | result_code |  | ['({host}[^\s\/]+)\/Security \(({result_code}({event_code}\d+))\)', 'Event(ID)?Code=({result_code}({event_code}\d+))', '\d\d:\d\d:\d\d \d\d\d\d\s*(\s|\t|,|#\d+|<[^>]+>)\s*({result_code}({event_code}\d+))\s*(\s|\t|,|#\d+|<[^>]+>)\s*Security'] |
| removed_attribute | DupFields |  | N/A |