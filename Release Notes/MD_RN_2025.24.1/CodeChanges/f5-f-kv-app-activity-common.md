# Code Changes for f5-f-kv-app-activity-common (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access_group', 'account', 'additional_info', 'bytes_in', 'bytes_out', 'dest_ip', 'dest_port', 'domain', 'email_address', 'end_time', 'host', 'object', 'os', 'realm', 'request', 'resource', 'result', 'result_code', 'session_id', 'src_host', 'src_ip', 'src_port', 'start_time', 'time', 'user', 'user_sid', 'vpn_server'] |
| edit_regex_field | vpn_server |  | ['\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d+:\d+\s({realm}({vpn_server}[^\s]+))'] |
| added_regex_field | realm |  | ['\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|-)\d+:\d+\s({realm}({vpn_server}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |