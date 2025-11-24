# Code Changes for cef-microsoft-app-activity1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'category', 'email_address', 'email_domain', 'event_hub_name', 'event_hub_namespace', 'full_name', 'host', 'location', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'result_code', 'server_name', 'severity', 'src_ip', 'src_port', 'subscription_id', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | object |  | ['"(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', '"\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| added_regex_field | resource |  | ['"(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', '"\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))', 'exa_regex="\_?(R|r)esourceId":\s*"({resource}({object}[^"]{1,249}))'] |
| removed_attribute | DupFields |  | N/A |