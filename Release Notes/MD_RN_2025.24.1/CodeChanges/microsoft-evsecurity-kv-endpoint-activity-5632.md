# Code Changes for microsoft-evsecurity-kv-endpoint-activity-5632 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'domain', 'event_code', 'event_name', 'failure_reason', 'host', 'login_id', 'result', 'result_code', 'result_reason', 'src_mac', 'ssid', 'time', 'user', 'user_sid'] |
| edit_regex_field | result_reason |  | ['Additional Information:\s*Reason Code:\s*({failure_reason}({result_reason}.+?))\s*Error Code:'] |
| added_regex_field | failure_reason |  | ['Additional Information:\s*Reason Code:\s*({failure_reason}({result_reason}.+?))\s*Error Code:'] |
| removed_attribute | DupFields |  | N/A |