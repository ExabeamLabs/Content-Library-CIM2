# Code Changes for checkpoint-ngfw-str-network-traffic-success-allow-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'email_address', 'email_domain', 'event_name', 'full_name', 'host', 'product_name', 'protocol', 'rule', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'user'] |
| edit_regex_field | action |  | ['logger:\s*\d\d:\d\d:\d\d\s*({event_name}({action}\w+))\s*({host}[\w.\-]+)'] |
| edit_regex_field | host |  | ['logger:\s*\d\d:\d\d:\d\d\s*({event_name}({action}\w+))\s*({host}[\w.\-]+)'] |
| added_regex_field | event_name |  | ['logger:\s*\d\d:\d\d:\d\d\s*({event_name}({action}\w+))\s*({host}[\w.\-]+)'] |
| removed_attribute | DupFields |  | N/A |