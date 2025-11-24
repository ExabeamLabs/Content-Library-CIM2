# Code Changes for microsoft-evsystem-kv-endpoint-notification-success-notification (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'account_name', 'attributes', 'domain', 'event_category', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'operation_type', 'result_code', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | account |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\\r\s\\r\s\\n)?Service Information:', 'Service Name(:|=)\s*(\w+\/(?=\w))?(\\t)+?(({account}[^\\\/"]+)[\\\/]+)?({domain}[^\\\/].+?)\s*;*(\\[rnt]|\s)*Network Information:', 'User="?(|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*"?\s'] |
| edit_regex_field | result_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}[\w]+))'] |
| edit_regex_field | user |  | ['Account Name(:|=)\s*(\\r|\\n|\\t)*?({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\\r\s\\r\s\\n)?Service Information:', 'User="?(|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*"?\s'] |
| added_regex_field | failure_code |  | ['Failure Code(:|=)\s*(\\r|\\n|\\t)*({failure_code}({result_code}[\w]+))'] |
| removed_attribute | DupFields |  | N/A |