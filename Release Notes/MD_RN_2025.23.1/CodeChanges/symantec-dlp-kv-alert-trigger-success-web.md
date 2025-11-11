# Code Changes for symantec-dlp-kv-alert-trigger-success-web (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'device_id', 'file_name', 'match_count', 'policy_name', 'protocol', 'result', 'src_host', 'src_ip', 'src_location', 'src_port', 'target', 'user'] |
| added_regex_field | result |  | ['\|\sRR_Action="({result}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |