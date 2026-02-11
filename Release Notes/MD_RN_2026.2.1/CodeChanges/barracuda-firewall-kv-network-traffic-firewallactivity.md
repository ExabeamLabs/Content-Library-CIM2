# Code Changes for barracuda-firewall-kv-network-traffic-firewallactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | action |  | ['\/box_Firewall_Activity:(\s+[-+][\d:\d]+)?\s+\w+\s+({host}[\w\-.]+)\s+({action}[^\s:]+):\s+(\w+=)?({event_code}[^\|\s]+?)\|'] |
| edit_regex_field | event_code |  | ['\/box_Firewall_Activity:(\s+[-+][\d:\d]+)?\s+\w+\s+({host}[\w\-.]+)\s+({action}[^\s:]+):\s+(\w+=)?({event_code}[^\|\s]+?)\|'] |
| edit_regex_field | host |  | ['\/box_Firewall_Activity:(\s+[-+][\d:\d]+)?\s+\w+\s+({host}[\w\-.]+)\s+({action}[^\s:]+):\s+(\w+=)?({event_code}[^\|\s]+?)\|'] |