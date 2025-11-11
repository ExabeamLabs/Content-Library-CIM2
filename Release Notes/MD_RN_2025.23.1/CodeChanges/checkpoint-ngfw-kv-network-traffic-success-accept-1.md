# Code Changes for checkpoint-ngfw-kv-network-traffic-success-accept-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'app_protocol', 'bytes_in', 'bytes_out', 'category', 'dest_domain', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'dest_user', 'direction', 'domain', 'email_address', 'email_domain', 'event_name', 'first_name', 'full_name', 'host', 'interface_name', 'last_name', 'origin_ip', 'origin_name', 'product_name', 'protocol', 'rule', 'rule_id', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'url', 'user', 'user_agent'] |
| added_regex_field | event_name |  | ['\Waction:"({event_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |