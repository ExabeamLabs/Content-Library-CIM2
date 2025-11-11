# Code Changes for hp-arubacpm-kv-radius-traffic-success-session-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'auth_server', 'dest_ip', 'dest_port', 'domain', 'failure_code', 'host', 'network', 'protocol', 'result_code', 'service_name', 'src_domain', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user', 'user_type'] |
| edit_regex_field | host |  | ['\s\d\d\s\d\d:\d\d:\d\d\s({auth_server}({host}[\w\.\-]+))\sLEEF:'] |
| edit_regex_field | result_code |  | ['Auth.Login-Status=(0|({failure_code}({result_code}\d+)))'] |
| added_regex_field | auth_server |  | ['\s\d\d\s\d\d:\d\d:\d\d\s({auth_server}({host}[\w\.\-]+))\sLEEF:'] |
| added_regex_field | failure_code |  | ['Auth.Login-Status=(0|({failure_code}({result_code}\d+)))'] |
| removed_attribute | DupFields |  | N/A |