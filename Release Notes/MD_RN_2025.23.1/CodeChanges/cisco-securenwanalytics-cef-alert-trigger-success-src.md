# Code Changes for cisco-securenwanalytics-cef-alert-trigger-success-src (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'host', 'host_ip', 'src_ip', 'src_port', 'time'] |
| added_regex_field | alert_type |  | ['CEF:([^\|]+\|){5}({alert_type}[^\|]+)'] |
| added_regex_field | event_name |  | ['CEF:([^\|]+\|){5}({event_name}[^\|]+)'] |
| removed_attribute | DupFields |  | N/A |