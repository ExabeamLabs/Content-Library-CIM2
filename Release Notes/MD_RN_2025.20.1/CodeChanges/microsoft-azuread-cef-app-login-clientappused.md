# Code Changes for microsoft-azuread-cef-app-login-clientappused (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'app_id', 'browser', 'correlation_id', 'country_code', 'device_class', 'device_description', 'device_id', 'device_name', 'device_type', 'domain', 'email_address', 'email_domain', 'error_code', 'event_subtype', 'failure_reason', 'first_name', 'full_name', 'last_name', 'location_city', 'location_state', 'object', 'operation', 'os', 'resource', 'result_reason', 'src_host', 'src_ip', 'src_port', 'status_msg', 'time', 'user', 'user_agent', 'user_upn'] |
| added_regex_field | device_class |  | ['\"deviceDetail\":\{[^\}]+?({device_class}"isCompliant":((?i)false|true))'] |
| added_regex_field | device_description |  | ['\"deviceDetail\":\{[^\}]+?({device_description}"isManaged":((?i)false|true))'] |