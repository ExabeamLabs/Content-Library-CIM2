# Code Changes for checkpoint-firewall-5 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'host', 'protocol', 'rule', 'src_host', 'src_ip', 'src_port', 'time'] |
| added_regex_field | alert_type |  | ['\Wmessage_info="({alert_type}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |