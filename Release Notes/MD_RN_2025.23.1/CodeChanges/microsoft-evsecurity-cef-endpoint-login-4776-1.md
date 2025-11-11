# Code Changes for microsoft-evsecurity-cef-endpoint-login-4776-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'event_code', 'event_id', 'event_name', 'failure_code', 'host', 'result', 'result_code', 'src_host', 'time', 'user', 'user_upn'] |
| edit_regex_field | result_code |  | ['"status":"({failure_code}({result_code}[^"]+?))\s*"'] |
| edit_regex_field | user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | dest_user |  | ['"targetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | failure_code |  | ['"status":"({failure_code}({result_code}[^"]+?))\s*"'] |
| removed_attribute | DupFields |  | N/A |