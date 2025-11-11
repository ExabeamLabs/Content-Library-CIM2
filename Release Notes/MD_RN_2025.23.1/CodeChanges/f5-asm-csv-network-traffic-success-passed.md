# Code Changes for f5-asm-csv-network-traffic-success-passed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_type', 'dest_ip', 'dest_port', 'host', 'method', 'protocol', 'referrer', 'severity', 'src_ip', 'src_port', 'time', 'user_agent', 'web_domain'] |
| edit_regex_field | protocol |  | ['\sASM:(\"[^\"]*\",){15}\"({alert_type}({protocol}[^\"]+))"', '\sASM:(\"[^\"]*\",){5}\"({alert_type}({protocol}[^\"]+))"'] |
| added_regex_field | alert_type |  | ['\sASM:(\"[^\"]*\",){15}\"({alert_type}({protocol}[^\"]+))"', '\sASM:(\"[^\"]*\",){5}\"({alert_type}({protocol}[^\"]+))"'] |
| removed_attribute | DupFields |  | N/A |