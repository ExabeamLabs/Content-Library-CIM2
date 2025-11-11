# Code Changes for okta-amfa-csv-app-login-success-securitycontext (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_domain', 'dest_email_address', 'dest_email_domain', 'dest_user', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'full_name', 'location_city', 'location_country', 'location_state', 'object', 'object_type', 'operation', 'operation_details', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | app |  | ['"type"+:"+AppInstance"+[^\}\]]*"displayName"+:"+({object}({app}[^"]+?))\s*"', '({object}({app}(?i)Okta))'] |
| edit_regex_field | operation |  | ['"eventType"+:"+({event_name}({operation}[^",]+))'] |
| added_regex_field | event_name |  | ['"eventType"+:"+({event_name}({operation}[^",]+))'] |
| added_regex_field | object |  | ['"type"+:"+AppInstance"+[^\}\]]*"displayName"+:"+({object}({app}[^"]+?))\s*"', '({object}({app}(?i)Okta))'] |
| removed_attribute | DupFields |  | N/A |