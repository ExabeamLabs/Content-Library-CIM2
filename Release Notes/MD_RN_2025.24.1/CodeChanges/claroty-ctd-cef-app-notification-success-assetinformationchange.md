# Code Changes for claroty-ctd-cef-app-notification-success-assetinformationchange (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'device_id', 'event_name', 'mitre_labels', 'operation', 'protocol', 'severity', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'url'] |
| added_regex_field | operation |  | ['\|Schneider\|CTD\|([^\|]+\|){2}({operation}[^\|]+)\|'] |
| removed_attribute | DupFields |  | N/A |