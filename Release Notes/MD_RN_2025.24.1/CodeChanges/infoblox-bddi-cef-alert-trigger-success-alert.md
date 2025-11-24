# Code Changes for infoblox-bddi-cef-alert-trigger-success-alert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'dns_query', 'host', 'operation', 'rule_id', 'src_ip', 'src_port', 'web_domain'] |
| edit_regex_field | operation |  | ['cat="({alert_type}({operation}[^"]+))'] |
| added_regex_field | alert_type |  | ['cat="({alert_type}({operation}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |