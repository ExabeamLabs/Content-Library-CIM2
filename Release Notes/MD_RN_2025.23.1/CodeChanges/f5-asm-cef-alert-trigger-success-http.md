# Code Changes for f5-asm-cef-alert-trigger-success-http (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'host', 'malware_url', 'protocol', 'referrer', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'web_domain'] |
| edit_regex_field | web_domain |  | ['Host:\s*({web_domain}[\w\-\.]+?)((\\r\\n|\s+)[\w\-]+:|\")'] |
| added_regex_field | referrer |  | ['Referer:\s*({referrer}[^"]+?)((\\r\\n|\s+)[\w\-]+:|\")'] |