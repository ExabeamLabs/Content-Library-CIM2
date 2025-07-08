# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4771-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['domain', 'event_code', 'host', 'result', 'result_code', 'service_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] | ['domain', 'event_code', 'event_name', 'host', 'result', 'result_code', 'service_name', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | event_name | [] | ['({event_name}Kerberos pre-authentication failed)'] |