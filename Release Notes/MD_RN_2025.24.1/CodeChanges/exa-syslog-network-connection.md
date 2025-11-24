# Code Changes for exa-syslog-network-connection (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'network', 'src_host', 'src_mac', 'ssid', 'user', 'wifiap'] |
| edit_regex_field | ssid |  | ['WLAN\[({network}({ssid}[^\]]+))'] |
| edit_regex_field | wifiap |  | ['AP\[({dest_host}({wifiap}[^@\]]+))'] |
| added_regex_field | dest_host |  | ['AP\[({dest_host}({wifiap}[^@\]]+))'] |
| added_regex_field | network |  | ['WLAN\[({network}({ssid}[^\]]+))'] |
| removed_attribute | DupFields |  | N/A |