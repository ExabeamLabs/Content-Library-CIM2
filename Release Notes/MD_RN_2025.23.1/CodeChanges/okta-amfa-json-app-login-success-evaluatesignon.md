# Code Changes for okta-amfa-json-app-login-success-evaluatesignon (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_severity', 'alert_type', 'app', 'domain', 'email_address', 'email_domain', 'event_name', 'failure_reason', 'full_name', 'object', 'operation', 'operation_details', 'result', 'time', 'user', 'user_agent'] |
| edit_regex_field | app |  | ['"type"+:"+AppInstance"+[^\}\]]*"displayName"+:"+({object}({app}[^"]+?))\s*"', '({object}({app}(O|o)kta))'] |
| added_regex_field | event_name |  | ['"eventType"+:"+({event_name}[^",]+)'] |
| added_regex_field | object |  | ['"type"+:"+AppInstance"+[^\}\]]*"displayName"+:"+({object}({app}[^"]+?))\s*"', '({object}({app}(O|o)kta))'] |
| removed_attribute | DupFields |  | N/A |