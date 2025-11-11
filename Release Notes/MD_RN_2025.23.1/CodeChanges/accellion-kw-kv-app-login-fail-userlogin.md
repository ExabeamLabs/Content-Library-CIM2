# Code Changes for accellion-kw-kv-app-login-fail-userlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'domain', 'email_address', 'email_domain', 'event_name', 'host', 'operation', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | event_name |  | ['Activity Type:\s({operation}({event_name}user_login_failed))'] |
| added_regex_field | operation |  | ['Activity Type:\s({operation}({event_name}user_login_failed))'] |
| removed_attribute | DupFields |  | N/A |