# Code Changes for f5-asm-cef-alert-trigger-success-cookie (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_type', 'dest_ip', 'dest_port', 'host', 'malware_url', 'method', 'protocol', 'referrer', 'result_reason', 'severity', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | protocol |  | ['\sASM:(\"[^\"]*\",){15}\"({alert_type}({protocol}[^\"]+))"', '\sASM:(\"[^\"]*\",){5}\"({alert_type}({protocol}[^\"]+))"'] |
| added_regex_field | alert_type |  | ['\sASM:(\"[^\"]*\",){15}\"({alert_type}({protocol}[^\"]+))"', '\sASM:(\"[^\"]*\",){5}\"({alert_type}({protocol}[^\"]+))"'] |
| removed_attribute | DupFields |  | N/A |