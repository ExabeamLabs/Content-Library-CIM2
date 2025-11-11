# Code Changes for hp-arubacpm-kv-radius-traffic-success-radiusaccounting (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_server', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'network', 'src_ip', 'src_port', 'time', 'user', 'user_type'] |
| added_regex_field | auth_server |  | ['\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d,\d+ ({auth_server}[\w\-.]+)'] |
| removed_attribute | DupFields |  | N/A |