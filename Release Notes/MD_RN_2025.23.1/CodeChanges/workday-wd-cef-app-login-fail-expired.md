# Code Changes for workday-wd-cef-app-login-fail-expired (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'auth_method', 'dproc', 'email_address', 'failure_reason', 'full_name', 'login_type_text', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | auth_method |  | ['\"+authenticationType\"+:\"+({login_type_text}({auth_method}[^\"]+))\"+', '\"authenticationChannel\"+:\"+({login_type_text}({auth_method}[^\"]+))'] |
| added_regex_field | login_type_text |  | ['\"+authenticationType\"+:\"+({login_type_text}({auth_method}[^\"]+))\"+', '\"authenticationChannel\"+:\"+({login_type_text}({auth_method}[^\"]+))'] |
| removed_attribute | DupFields |  | N/A |