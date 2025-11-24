# Code Changes for microsoft-evsecurity-kv-endpoint-login-success-4771 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'result_code', 'run_level', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | account |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\\r\s\\r\s\\n)?Service Information:', 'Account Name(:|=)\s*(\\r|\\n|\\t)*?({account}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\r\s\\r\s\\n)*', 'Service Name(:|=)\s*(\w+\/(?=\w))?(\\t)+?(({account}[^\\\/"]+)[\\\/]+)?({domain}[^\\\/].+?)\s*;*(\\[rnt]|\s)*Network Information:'] |
| edit_regex_field | result_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}[\w]+))'] |
| edit_regex_field | user |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\\r\s\\r\s\\n)?Service Information:', 'Account Name(:|=)\s*(\\r|\\n|\\t)*?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*(\\r\s\\r\s\\n)*'] |
| added_regex_field | failure_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}[\w]+))'] |
| removed_attribute | DupFields |  | N/A |