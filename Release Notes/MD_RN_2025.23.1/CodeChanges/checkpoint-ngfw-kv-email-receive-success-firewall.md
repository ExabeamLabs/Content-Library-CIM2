# Code Changes for checkpoint-ngfw-kv-email-receive-success-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'app_protocol', 'bytes_in', 'bytes_out', 'dest_host', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'direction', 'domain', 'email_address', 'email_domain', 'event_name', 'first_name', 'host', 'interface_name', 'last_name', 'num_recipients', 'origin_ip', 'origin_name', 'product_name', 'protocol', 'result', 'rule', 'rule_id', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'user'] |
| added_regex_field | event_name |  | ['\Waction:"({event_name}[^"]+)'] |
| added_regex_field | result |  | ['\Waction:"({result}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |