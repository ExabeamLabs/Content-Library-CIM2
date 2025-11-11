# Code Changes for hp-arubacpm-kv-radius-traffic-fail-authenticationfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_method', 'auth_server', 'dest_ip', 'domain', 'event_code', 'failure_reason', 'host', 'network', 'src_domain', 'src_host', 'src_mac', 'time', 'user', 'user_type'] |
| added_regex_field | auth_server |  | ['\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({auth_server}[\w\-.]+)'] |
| removed_attribute | DupFields |  | N/A |