# Code Changes for microsoft-azuresc-sk4-alert-trigger-success-asc (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_subject', 'alert_type', 'domain', 'email_address', 'full_name', 'host', 'incident_status', 'malware_url', 'provider_name', 'src_host', 'src_ip', 'src_location', 'src_port', 'subscription_id', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['"title":"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |
| added_regex_field | alert_subject |  | ['"title":"({alert_subject}({alert_name}[^"]+?))(\\u200b)?"'] |
| removed_attribute | DupFields |  | N/A |