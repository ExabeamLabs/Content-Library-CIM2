# Code Changes for imperva-securesphere-leef-alert-trigger-success-alertdescription (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'server_group', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_type |  | ['(\s|\|)Alert type=({alert_name}({alert_type}[^\|]+))'] |
| added_regex_field | alert_name |  | ['(\s|\|)Alert type=({alert_name}({alert_type}[^\|]+))'] |
| removed_attribute | DupFields |  | N/A |