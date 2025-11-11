# Code Changes for microsoft-o365-cef-app-login-fail-userloginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_id', 'browser', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_code', 'failure_reason', 'object', 'object_id', 'operation', 'os', 'request_type', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_id', 'user_type', 'user_upn'] |
| edit_regex_field | error_code |  | ['"ErrorNumber":\s*"({failure_code}({error_code}\d+))"'] |
| added_regex_field | failure_code |  | ['"ErrorNumber":\s*"({failure_code}({error_code}\d+))"'] |
| removed_attribute | DupFields |  | N/A |