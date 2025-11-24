# Code Changes for microsoft-azuremon-sk4-app-notification-resourcehealth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'category', 'email_address', 'email_domain', 'event_category', 'event_hub_name', 'event_hub_namespace', 'event_name', 'full_name', 'host', 'location', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'result', 'result_code', 'result_reason', 'server_name', 'severity', 'src_ip', 'src_port', 'subscription_id', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | object |  | ['"(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', '"\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| added_regex_field | resource |  | ['"(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', '"\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| removed_attribute | DupFields |  | N/A |