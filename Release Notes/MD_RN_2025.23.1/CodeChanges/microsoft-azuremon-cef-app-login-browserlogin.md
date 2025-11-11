# Code Changes for microsoft-azuremon-cef-app-login-browserlogin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'category', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'full_name', 'host', 'object', 'operation', 'resource', 'result_code', 'src_ip', 'src_port', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | object |  | ['"resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| added_regex_field | resource |  | ['"resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| removed_attribute | DupFields |  | N/A |