# Code Changes for microsoft-o365-cef-app-login-fail-userloginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['app', 'app_id', 'browser', 'email_address', 'error_code', 'event_name', 'failure_reason', 'object', 'object_id', 'operation', 'os', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user_agent', 'user_type', 'user_upn'] | ['app', 'app_id', 'browser', 'email_address', 'error_code', 'event_name', 'failure_reason', 'object', 'object_id', 'operation', 'os', 'request_type', 'resource', 'result', 'src_ip', 'src_port', 'time', 'user_agent', 'user_type', 'user_upn'] |
| added_regex_field | request_type | [] | ['"Name":"RequestType","Value":"({request_type}[^"]+?)\s*"', '"Value":"({request_type}[^"]+?)\s*","Name":"RequestType"'] |