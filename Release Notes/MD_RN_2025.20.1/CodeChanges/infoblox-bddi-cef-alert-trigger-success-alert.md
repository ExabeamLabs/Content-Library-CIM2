# Code Changes for infoblox-bddi-cef-alert-trigger-success-alert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'dest_ip', 'dest_port', 'dns_query', 'host', 'operation', 'rule_id', 'src_ip', 'src_port', 'web_domain'] |
| removed_regex_field | src_host |  | [] |
| added_regex_field | dns_query |  | ['fqdn=(((?i)na\s)|({dns_query}[\w\-.]+))'] |