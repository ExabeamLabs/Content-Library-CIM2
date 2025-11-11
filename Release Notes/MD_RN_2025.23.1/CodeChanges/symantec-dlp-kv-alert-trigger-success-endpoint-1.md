# Code Changes for symantec-dlp-kv-alert-trigger-success-endpoint-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_email_address', 'device_id', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'file_name', 'match_count', 'policy_name', 'protocol', 'result', 'src_host', 'src_ip', 'src_location', 'src_port', 'target', 'time', 'user'] |
| added_regex_field | result |  | ['\|\sRR_Action="({result}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |