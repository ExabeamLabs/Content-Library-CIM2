# Code Changes for cisco-firepower-json-app-activity-appactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'dest_ip', 'dest_port', 'event_name', 'policy_name', 'sensor', 'src_ip', 'src_port', 'time'] |
| added_regex_field | alert_name |  | ['\WrecordTypeDescription":\s*"({alert_name}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |