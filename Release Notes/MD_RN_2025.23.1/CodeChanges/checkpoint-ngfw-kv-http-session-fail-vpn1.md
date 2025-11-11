# Code Changes for checkpoint-ngfw-kv-http-session-fail-vpn1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'dest_ip', 'dest_port', 'event_name', 'host', 'product_name', 'rule', 'src_ip', 'src_port', 'src_translated_ip', 'time', 'user'] |
| added_regex_field | event_name |  | ['https_inspection_action="({event_name}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |