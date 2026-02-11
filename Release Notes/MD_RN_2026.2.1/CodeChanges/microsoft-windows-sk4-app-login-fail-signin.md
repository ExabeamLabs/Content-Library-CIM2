# Code Changes for microsoft-windows-sk4-app-login-fail-signin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'attribute', 'auth_method', 'browser', 'category', 'city', 'country_code', 'device_id', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_code', 'failure_reason', 'first_name', 'full_name', 'last_name', 'location', 'operation', 'os', 'principal_id', 'resource', 'result', 'severity', 'src_host', 'src_ip', 'src_network_type', 'src_network_zone', 'src_port', 'state', 'time', 'user_agent', 'user_id'] |
| added_regex_field | src_network_type |  | ['"networkType":\s*"({src_network_type}[^"]+)"'] |
| added_regex_field | src_network_zone |  | ['"networkNames":\s*\["({src_network_zone}[^"]+)"'] |