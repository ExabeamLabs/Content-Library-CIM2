# Code Changes for google-gcp-sk4-alert-trigger-success-securitycenter (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'email_address', 'email_domain', 'event_name', 'resource_path', 'time', 'url'] |
| edit_regex_field | alert_name |  | ['category:\s*"({event_name}({alert_name}[^"]+))'] |
| added_regex_field | event_name |  | ['category:\s*"({event_name}({alert_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |