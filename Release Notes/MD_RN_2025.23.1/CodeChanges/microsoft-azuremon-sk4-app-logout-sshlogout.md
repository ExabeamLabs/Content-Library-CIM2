# Code Changes for microsoft-azuremon-sk4-app-logout-sshlogout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'browser', 'category', 'correlation_id', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'full_name', 'host', 'http_response_code', 'object', 'operation', 'os', 'resource', 'src_ip', 'src_port', 'time', 'user_agent', 'user_type', 'user_upn'] |
| edit_regex_field | object |  | ['resourceId":\s*"({resource}({object}[^"]+))'] |
| added_regex_field | resource |  | ['resourceId":\s*"({resource}({object}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |