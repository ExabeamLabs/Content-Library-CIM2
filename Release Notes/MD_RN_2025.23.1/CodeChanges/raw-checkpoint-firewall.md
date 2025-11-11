# Code Changes for raw-checkpoint-firewall (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'dest_ip', 'dest_port', 'dest_translated_ip', 'dest_translated_port', 'email_address', 'event_name', 'full_name', 'host', 'policy_name', 'product_name', 'protocol', 'rule', 'src_ip', 'src_port', 'src_translated_ip', 'src_translated_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\s({host}[\w\-\.]+)\s+product:\s*VPN-1 & FireWall-1;', 'logger:\s*\d\d:\d\d:\d\d\s*({action}\w+)\s*({host}[\w.\-]+)', 'logger:\s*\d\d:\d\d:\d\d\s*({event_name}\w+)\s*({host}[\w.\-]+)'] |
| added_regex_field | event_name |  | ['\s({event_name}\w+)\s+\S+\s+product:\s*VPN-1 & FireWall-1;', 'logger:\s*\d\d:\d\d:\d\d\s*({event_name}\w+)\s*({host}[\w.\-]+)'] |
| removed_attribute | DupFields |  | N/A |