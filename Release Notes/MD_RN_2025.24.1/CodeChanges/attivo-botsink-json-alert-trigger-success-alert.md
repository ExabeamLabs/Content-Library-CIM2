# Code Changes for attivo-botsink-json-alert-trigger-success-alert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'category', 'src_host', 'src_ip', 'time'] |
| edit_regex_field | alert_name |  | ['"subject":\s*"({alert_subject}({alert_name}[^"]+))"'] |
| added_regex_field | alert_subject |  | ['"subject":\s*"({alert_subject}({alert_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |