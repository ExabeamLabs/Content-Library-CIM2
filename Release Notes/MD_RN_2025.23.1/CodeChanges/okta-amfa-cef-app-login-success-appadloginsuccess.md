# Code Changes for okta-amfa-cef-app-login-success-appadloginsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'app_id', 'auth_method', 'browser', 'device_type', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'fingerprint', 'first_name', 'full_name', 'hash_sha256', 'last_name', 'location_city', 'location_country', 'location_state', 'mfa_country', 'more_info', 'object', 'operation', 'operation_details', 'operator_name', 'os', 'response_type', 'result', 'result_reason', 'severity', 'src_ip', 'src_port', 'time', 'uri_path', 'user', 'user_agent'] |
| edit_regex_field | additional_info |  | ['"reason":"({additional_info}({failure_reason}[^"]+))', '"risk":"\{reasons=({additional_info}({failure_reason}[^=]+?)),\s\w+=', '"tunnels":"\[({additional_info}([^,]+,\\"operator\\":(null|\\"({operator_name}[^\\"]+)))?[^\]]+)', 'exa_json_path=$.debugContext.debugData.risk,exa_regex=^\{reasons=({additional_info}[^=]+?),\s\w+=', 'exa_regex="tunnels":"\[({additional_info}([^,]+,\\"operator\\":(null|\\"({operator_name}[^\\"]+)))?[^\]]+)'] |
| edit_regex_field | failure_reason |  | ['"reason":"({additional_info}({failure_reason}[^"]+))', '"risk":"\{reasons=({additional_info}({failure_reason}[^=]+?)),\s\w+=', 'exa_json_path=$.debugContext.debugData.risk,exa_regex=^\{reasons=({failure_reason}[^=]+?),\s\w+='] |
| edit_regex_field | location_country |  | ['"country":"({mfa_country}({location_country}[^",]+))'] |
| added_regex_field | mfa_country |  | ['"country":"({mfa_country}({location_country}[^",]+))'] |
| removed_attribute | DupFields |  | N/A |