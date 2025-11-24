# Code Changes for trendmicro-ds-leef-endpoint-activity-success-integritymonitor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'event_name', 'file_dir', 'file_name', 'file_path', 'host', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['\Wname=({event_name}({alert_name}.+?))\s*(\w+=|$)'] |
| added_regex_field | event_name |  | ['\Wname=({event_name}({alert_name}.+?))\s*(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |