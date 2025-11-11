# Code Changes for symantec-dlp-kv-alert-trigger-success-riskseverity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'email_address', 'first_name', 'host', 'last_name', 'time', 'user'] |
| added_regex_field | alert_type |  | [', violatedPolicyRuleName:\s*({alert_type}[^\],]+?)\s*,'] |
| removed_attribute | DupFields |  | N/A |