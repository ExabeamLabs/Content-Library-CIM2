# Code Changes for cisco-ios-str-alert-trigger-success-snoopingdeny (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'dest_ip', 'dest_port', 'event_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | event_name |  | ['({alert_name}({event_name}DHCP_SNOOPING_DENY))'] |
| added_regex_field | alert_name |  | ['({alert_name}({event_name}DHCP_SNOOPING_DENY))'] |
| removed_attribute | DupFields |  | N/A |