# Code Changes for pingidentity-pi-str-endpoint-login-success-stssuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_method', 'email_address', 'email_domain', 'host', 'host_ip', 'protocol', 'result', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | protocol |  | ['(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({auth_method}({protocol}[^\s\|]+))'] |
| added_regex_field | auth_method |  | ['(\|\s*(AUTHN_ATTEMPT|OAuth|SSO|AUTHN_SESSION_CREATED|AUTHN_SESSION_USED|STS)\s*\|)\s*([^\|]*\|){4}\s*({auth_method}({protocol}[^\s\|]+))'] |
| removed_attribute | DupFields |  | N/A |