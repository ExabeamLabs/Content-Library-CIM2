# Code Changes for okta-amfa-mix-app-login-fail-suspiciousactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'app', 'email_address', 'email_domain', 'first_name', 'last_name', 'more_info', 'operation', 'result', 'src_ip', 'src_port'] |
| added_regex_field | more_info |  | ['exa_regex=behaviors":"\{({more_info}[^\}]+)'] |