# Code Changes for microsoft-evsecurity-cef-endpoint-login-fail-4771 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'event_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'location', 'result_code', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | result_code |  | ['\scs4=({failure_code}({result_code}[^\s]+))'] |
| added_regex_field | failure_code |  | ['\scs4=({failure_code}({result_code}[^\s]+))'] |
| removed_attribute | DupFields |  | N/A |