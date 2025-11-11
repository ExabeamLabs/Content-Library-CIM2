# Code Changes for f5-asm-cef-alert-trigger-success-cookie-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'host', 'malware_url', 'protocol', 'time', 'user_agent', 'web_domain'] |
| removed_regex_field | domain |  | [] |
| edit_regex_field | malware_url |  | ['\sASM:("[^"]*",){6}"\w+\s+({malware_url}[^"]+?)\s+(({alert_type}({protocol}\w+))\/\d\.\d|)((\\r\\n|\s+)[\w\-]+:|")'] |
| edit_regex_field | protocol |  | ['\sASM:("[^"]*",){6}"\w+\s+({malware_url}[^"]+?)\s+(({alert_type}({protocol}\w+))\/\d\.\d|)((\\r\\n|\s+)[\w\-]+:|")'] |
| added_regex_field | alert_type |  | ['\sASM:("[^"]*",){6}"\w+\s+({malware_url}[^"]+?)\s+(({alert_type}({protocol}\w+))\/\d\.\d|)((\\r\\n|\s+)[\w\-]+:|")'] |
| added_regex_field | web_domain |  | ['(\\r\\n|\s)Host:\s*({web_domain}[^"]+?)((\\r\\n|\s+)[\w\-]+:|")'] |
| removed_attribute | DupFields |  | N/A |