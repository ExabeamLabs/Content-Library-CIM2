# Code Changes for infoblox-bddi-cef-alert-trigger-success-alert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'dest_ip', 'dest_port', 'host', 'operation', 'rule_id', 'src_host', 'src_ip', 'src_port', 'web_domain'] |
| removed_regex_field | top_domain |  | [] |
| added_regex_field | web_domain |  | ['fqdn=((?i)NA|({web_domain}[^\s]+))\s*'] |