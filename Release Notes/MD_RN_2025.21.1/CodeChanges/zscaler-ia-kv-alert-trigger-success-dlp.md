# Code Changes for zscaler-ia-kv-alert-trigger-success-dlp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'browser', 'dest_ip', 'dest_port', 'domain', 'email_address', 'host', 'protocol', 'result', 'src_ip', 'src_port', 'target', 'time', 'user', 'user_agent'] |
| edit_regex_field | user_agent |  | ['\suseragent=({browser}({user_agent}.+?))\s+(\w+=|$)'] |
| added_regex_field | browser |  | ['\suseragent=({browser}({user_agent}.+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |