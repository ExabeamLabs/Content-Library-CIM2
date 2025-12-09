# Code Changes for cisco-duo-cef-endpoint-authentication-newenrollment (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'auth_method', 'browser', 'city', 'country', 'device_name', 'domain', 'email_address', 'email_domain', 'event_name', 'factor', 'failure_reason', 'full_name', 'host', 'mfa_country', 'mfa_device', 'new_enrollment', 'object', 'operation', 'os', 'result', 'service_name', 'src_ip', 'src_port', 'state', 'time', 'user'] |
| edit_regex_field | app |  | ['\"integration\":\s*\"({service_name}({app}[^\"]+))'] |
| edit_regex_field | country |  | ['\"country\":\s*\"({mfa_country}({country}[^\"]+))'] |
| edit_regex_field | object |  | ['\"device\":\s*\"({mfa_device}({device_name}({object}[^\"]+)))'] |
| edit_regex_field | operation |  | ['\"factor\":\s*\"(?:(n\/a)|({factor}({auth_method}({operation}[^\"]+))))\"'] |
| edit_regex_field | result |  | ['\"result\":\s*\"({action}({result}[^\"]+))'] |
| added_regex_field | action |  | ['\"result\":\s*\"({action}({result}[^\"]+))'] |
| added_regex_field | auth_method |  | ['\"factor\":\s*\"(?:(n\/a)|({factor}({auth_method}({operation}[^\"]+))))\"'] |
| added_regex_field | device_name |  | ['\"device\":\s*\"({mfa_device}({device_name}({object}[^\"]+)))'] |
| added_regex_field | factor |  | ['\"factor\":\s*\"(?:(n\/a)|({factor}({auth_method}({operation}[^\"]+))))\"'] |
| added_regex_field | mfa_country |  | ['\"country\":\s*\"({mfa_country}({country}[^\"]+))'] |
| added_regex_field | mfa_device |  | ['\"device\":\s*\"({mfa_device}({device_name}({object}[^\"]+)))'] |
| added_regex_field | service_name |  | ['\"integration\":\s*\"({service_name}({app}[^\"]+))'] |
| removed_attribute | DupFields |  | N/A |