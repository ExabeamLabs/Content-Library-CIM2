# Code Changes for symantec-endpointprotection-json-alert-trigger-success-8040 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'app', 'domain', 'event_code', 'host', 'operation', 'os', 'session_id', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_uid'] |
| added_regex_field | src_host |  | ['"device_name":"({src_host}[\w\-.]+)'] |
| removed_attribute | DupFields |  | N/A |