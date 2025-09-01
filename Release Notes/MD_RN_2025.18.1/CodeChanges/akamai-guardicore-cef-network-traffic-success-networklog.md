# Code Changes for akamai-guardicore-cef-network-traffic-success-networklog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'category', 'connection_type', 'dest_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'event_name', 'protocol', 'src_host', 'src_ip', 'src_port', 'time'] |
| removed_regex_field | web_domain |  | [] |
| added_regex_field | connection_type |  | ['cs1=({connection_type}[^\s]+)\s+\w+='] |
| added_regex_field | dest_host |  | ['dhost=({dest_host}[\w\-\.]+)'] |
| added_regex_field | src_host |  | ['shost=({src_host}[\w\-\.]+)'] |