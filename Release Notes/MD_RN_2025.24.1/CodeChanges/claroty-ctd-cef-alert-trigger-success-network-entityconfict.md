# Code Changes for claroty-ctd-cef-alert-trigger-success-network-entityconfict (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'event_name', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['\|CTD\|([^\|]+\|){2}({alert_type}({event_name}({alert_name}[^\|]+)))\|({alert_severity}[^\|]+)'] |
| edit_regex_field | alert_severity |  | ['\|CTD\|([^\|]+\|){2}({alert_type}({event_name}({alert_name}[^\|]+)))\|({alert_severity}[^\|]+)'] |
| added_regex_field | alert_type |  | ['\|CTD\|([^\|]+\|){2}({alert_type}({event_name}({alert_name}[^\|]+)))\|({alert_severity}[^\|]+)'] |
| added_regex_field | event_name |  | ['\|CTD\|([^\|]+\|){2}({alert_type}({event_name}({alert_name}[^\|]+)))\|({alert_severity}[^\|]+)'] |
| removed_attribute | DupFields |  | N/A |