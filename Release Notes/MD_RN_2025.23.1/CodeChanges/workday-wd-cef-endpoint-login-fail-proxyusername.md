# Code Changes for workday-wd-cef-endpoint-login-fail-proxyusername (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_method', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'full_name', 'login_type_text', 'time', 'user'] |
| edit_regex_field | auth_method |  | ['authenticationType"+:"+({login_type_text}({auth_method}[^"]+))'] |
| added_regex_field | login_type_text |  | ['authenticationType"+:"+({login_type_text}({auth_method}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |