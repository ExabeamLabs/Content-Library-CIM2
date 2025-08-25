# Code Changes for okta-amfa-mix-app-login-success-securitycontext (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_severity', 'alert_type', 'app', 'app_id', 'auth_method', 'browser', 'dest_user_full_name', 'device_name', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'fingerprint', 'first_name', 'full_name', 'group_name', 'last_name', 'location_city', 'location_country', 'location_state', 'more_info', 'object', 'object_type', 'operation', 'operation_details', 'operator_name', 'os', 'result', 'result_reason', 'severity', 'src_ip', 'src_port', 'src_user', 'target', 'time', 'uri_path', 'user', 'user_agent'] |
| edit_regex_field | more_info |  | ['"behaviors":"\{({more_info}[^\}"]+)\}"', '"behaviors\\*":"*\{({more_info}[^\}]+)', 'exa_regex=behaviors\\*":"*\{({more_info}[^\}]+)'] |
| added_regex_field | device_name |  | ['"target":[^\]]+?"type":"UDDevice"[^\]]+?"displayName":"({device_name}[^"]+)",', 'exa_regex="target":[^\]]+?"type":"UDDevice"[^\]]+?"displayName":"({device_name}[^"]+)",'] |