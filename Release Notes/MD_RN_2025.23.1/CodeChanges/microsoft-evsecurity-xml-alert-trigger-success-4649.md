# Code Changes for microsoft-evsecurity-xml-alert-trigger-success-4649 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_id', 'additional_info', 'alert_name', 'alert_type', 'auth_process', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'process_id', 'provider_name', 'result', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | auth_process |  | ['Name=(\'|")LogonProcessName\'>({alert_type}({auth_process}[^<]+))'] |
| edit_regex_field | event_name |  | ['<Message>({alert_name}({event_name}.+?))\s*\.(\s|</Message>)', '<Message>({alert_name}({event_name}.+?))\s+Subject:'] |
| added_regex_field | alert_name |  | ['<Message>({alert_name}({event_name}.+?))\s*\.(\s|</Message>)', '<Message>({alert_name}({event_name}.+?))\s+Subject:'] |
| added_regex_field | alert_type |  | ['Name=(\'|")LogonProcessName\'>({alert_type}({auth_process}[^<]+))'] |
| removed_attribute | DupFields |  | N/A |