# Code Changes for okta-amfa-json-app-login-success-evaluatesignon-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'app_id', 'browser', 'dest_host', 'device_id', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'fingerprint', 'first_name', 'full_name', 'hash_sha256', 'identity_type', 'last_name', 'location_city', 'location_country', 'location_state', 'more_info', 'operation', 'operation_details', 'os', 'os_version', 'result', 'result_reason', 'severity', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | additional_info |  | ['"displayMessage":"({additional_info}[^"]+)'] |
| added_regex_field | more_info |  | ['"behaviors\\*":"*\{({more_info}[^\}]+)', 'exa_regex=behaviors\\*":"*\{({more_info}[^\}]+)'] |