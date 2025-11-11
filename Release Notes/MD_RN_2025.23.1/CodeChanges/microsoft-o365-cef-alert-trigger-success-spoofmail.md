# Code Changes for microsoft-o365-cef-alert-trigger-success-spoofmail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_type', 'direction', 'email_domain', 'external_domain', 'operation', 'src_ip', 'time', 'user'] |
| edit_regex_field | alert_type |  | ['"EventType":"({alert_name}({alert_type}[^"]+))"'] |
| added_regex_field | alert_name |  | ['"EventType":"({alert_name}({alert_type}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |