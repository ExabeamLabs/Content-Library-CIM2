# Code Changes for f5-asm-cef-alert-trigger-success-http (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'host', 'malware_url', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'web_domain'] |
| removed_regex_field | top_domain |  | [] |
| edit_regex_field | web_domain |  | ['cs3=[^\]]+?Host:\s*({web_domain}[^\.:]+\.([^\/\.\s":]+\.\w+))'] |