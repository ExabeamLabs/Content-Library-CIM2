# Code Changes for okta-amfa-cef-app-login-success-coreuserauthloginsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'app_id', 'auth_method', 'browser', 'device_id', 'device_type', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'fingerprint', 'first_name', 'full_name', 'hash_sha256', 'identity_type', 'last_name', 'location_city', 'location_country', 'location_state', 'more_info', 'object', 'operation', 'operation_details', 'operator_name', 'os', 'os_version', 'response_type', 'result', 'result_reason', 'serial_num', 'severity', 'src_ip', 'src_port', 'time', 'uri_path', 'user', 'user_agent'] |
| added_regex_field | serial_num |  | ['exa_regex=serialNumber\\*":\\*"({serial_num}[^"\\]+)\\*"', 'serialNumber\\*":\\*"({serial_num}[^"\\]+)\\*"'] |