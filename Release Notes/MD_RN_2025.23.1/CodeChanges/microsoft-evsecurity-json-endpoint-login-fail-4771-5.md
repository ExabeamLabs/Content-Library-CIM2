# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4771-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'failure_code', 'host', 'result', 'result_code', 'service_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | result_code |  | ['"Status":"({failure_code}({result_code}[^"]+))"'] |
| edit_regex_field | user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user_sid |  | ['"TargetSid":"({dest_user_sid}({user_sid}[^"]+))"'] |
| added_regex_field | dest_user |  | ['"TargetUserName":"({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_user_sid |  | ['"TargetSid":"({dest_user_sid}({user_sid}[^"]+))"'] |
| added_regex_field | failure_code |  | ['"Status":"({failure_code}({result_code}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |