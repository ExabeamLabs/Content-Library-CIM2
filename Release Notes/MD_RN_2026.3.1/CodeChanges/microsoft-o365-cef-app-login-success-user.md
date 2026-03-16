# Code Changes for microsoft-o365-cef-app-login-success-user (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'app_id', 'browser', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'first_name', 'full_name', 'last_name', 'object', 'object_id', 'operation', 'os', 'request_type', 'result', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user_agent', 'user_sid', 'user_type', 'user_upn'] |
| added_regex_field | session_id |  | ['\{"Value":"({session_id}[^",]+)","Name":"SessionId"', 'exa_regex=\{"Value":"({session_id}[^",]+)","Name":"SessionId"'] |