# Code Changes for symantec-dlp-kv-alert-trigger-success-incidentid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'email_address', 'email_domain', 'src_host', 'target', 'time', 'user'] |
| added_regex_field | alert_type |  | ['policy="({alert_type}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |