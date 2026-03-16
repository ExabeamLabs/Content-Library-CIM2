# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-adaudit-4771 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_id', 'event_name', 'failure_code', 'failure_reason', 'host', 'result', 'result_code', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | user_sid |  | ['USER_SID\s*=\s*(\%\{)?({user_sid}[^\}\s\]]+)'] |
| added_regex_field | event_name |  | ['({event_name}Kerberos pre-authentication failed)'] |
| added_regex_field | failure_reason |  | ['ERROR_CODE_TEXT\s*=\s*({failure_reason}.+?)\s*\]'] |