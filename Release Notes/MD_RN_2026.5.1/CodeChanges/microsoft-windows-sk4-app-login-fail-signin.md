# Code Changes for microsoft-windows-sk4-app-login-fail-signin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'attribute', 'auth', 'auth_method', 'browser', 'category', 'city', 'country_code', 'device_id', 'device_name', 'email_address', 'email_domain', 'error_code', 'event_name', 'failure_code', 'failure_reason', 'first_name', 'full_name', 'last_name', 'location', 'operation', 'os', 'principal_id', 'resource', 'result', 'session_id', 'severity', 'src_ip', 'src_network_type', 'src_network_zone', 'src_port', 'state', 'tenant_id', 'time', 'user_agent', 'user_id'] |
| edit_regex_field | auth_method |  | ['"authMethod":"({auth_method}[^"]+)"', '"authenticationMethod\\*":\\*"({auth_method}[^\\"]+)\\*"', '"authenticationProtocol\\*":\\*"(none|({auth_method}[^\\"]+))\\*"', 'exa_regex="authenticationProtocol\\*":\\*"(none|({auth_method}[^\\"]+))\\*"'] |
| removed_regex_field | src_host |  | [] |
| added_regex_field | auth |  | ['"AuthenticationRequirement":"({auth}[^"]+)"'] |
| added_regex_field | device_name |  | ['deviceDetail(_string)?\\*":"?\{[^\}]*"displayName\\*":\\*"({device_name}[^",]+)\$?\s*\\*', 'exa_regex=deviceDetail(_string)?\\*":"?\{[^\}]*"displayName\\*":\\*"({device_name}[^",]+)\$?\s*\\*', 'exa_regex=deviceDetail\".+?"deviceId":"[^"]+".+?"displayName":"({device_name}[^",]+)"'] |