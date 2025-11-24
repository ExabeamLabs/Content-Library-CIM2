# Code Changes for akamai-guardicore-cef-alert-trigger-success-revealincident (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'description', 'dest_host', 'dest_ip', 'dest_port', 'event_name', 'more_info', 'protocol', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | category |  | ['CEF:\d+\|([^\|]+\|){4}({alert_type}({category}[^\|]+))'] |
| edit_regex_field | event_name |  | ['CEF:\d+\|([^\|]+\|){3}({alert_name}({event_name}[^\|]+))'] |
| added_regex_field | alert_name |  | ['CEF:\d+\|([^\|]+\|){3}({alert_name}({event_name}[^\|]+))'] |
| added_regex_field | alert_type |  | ['CEF:\d+\|([^\|]+\|){4}({alert_type}({category}[^\|]+))'] |
| removed_attribute | DupFields |  | N/A |