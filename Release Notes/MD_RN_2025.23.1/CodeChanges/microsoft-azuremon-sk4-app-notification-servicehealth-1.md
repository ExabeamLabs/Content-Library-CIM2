# Code Changes for microsoft-azuremon-sk4-app-notification-servicehealth-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'category', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'dest_user', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'failure_reason', 'host', 'location', 'object', 'operation', 'resource', 'resource_group', 'resource_id', 'result', 'result_code', 'server_name', 'service_name', 'severity', 'src_ip', 'src_mac', 'src_port', 'subscription_id', 'tenant_id', 'time', 'user', 'user_agent', 'user_id', 'user_type'] |
| edit_regex_field | additional_info |  | ['"description":\s*"({failure_reason}({additional_info}[^"]+))', '"message":\s*"({failure_reason}({additional_info}[^"]+))', 'exa_regex=message":\s*"({failure_reason}({additional_info}[^"]+))'] |
| edit_regex_field | object |  | ['"(?i)resourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex=(?i)resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| added_regex_field | failure_reason |  | ['"description":\s*"({failure_reason}({additional_info}[^"]+))', '"message":\s*"({failure_reason}({additional_info}[^"]+))', 'exa_regex=message":\s*"({failure_reason}({additional_info}[^"]+))'] |
| added_regex_field | resource |  | ['"(?i)resourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex=(?i)resourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| removed_attribute | DupFields |  | N/A |