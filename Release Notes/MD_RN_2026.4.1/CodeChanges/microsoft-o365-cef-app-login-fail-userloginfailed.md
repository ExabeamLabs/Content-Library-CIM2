# Code Changes for microsoft-o365-cef-app-login-fail-userloginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_id', 'browser', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_code', 'failure_reason', 'host', 'object', 'object_id', 'operation', 'os', 'request_type', 'resource', 'result', 'session_id', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'user_id', 'user_type', 'user_upn'] |
| added_regex_field | host |  | ['"DeviceProperties":.+?"DisplayName",\s*"Value":\s*"({host}[\w\-.]+)"'] |