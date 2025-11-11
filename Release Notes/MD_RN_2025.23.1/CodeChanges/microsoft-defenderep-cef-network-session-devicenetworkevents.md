# Code Changes for microsoft-defenderep-cef-network-session-devicenetworkevents (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'event_name', 'full_name', 'host', 'operation', 'process_dir', 'process_integrity', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'user', 'user_sid', 'web_domain'] |
| edit_regex_field | category |  | ['({event_name}({category}AdvancedHunting-DeviceNetworkEvents))', 'category"+:\s*"+({event_name}({category}[^"]+))', 'exa_regex=({event_name}({category}AdvancedHunting-DeviceNetworkEvents))'] |
| added_regex_field | event_name |  | ['({event_name}({category}AdvancedHunting-DeviceNetworkEvents))', 'category"+:\s*"+({event_name}({category}[^"]+))', 'exa_regex=({event_name}({category}AdvancedHunting-DeviceNetworkEvents))'] |
| removed_attribute | DupFields |  | N/A |