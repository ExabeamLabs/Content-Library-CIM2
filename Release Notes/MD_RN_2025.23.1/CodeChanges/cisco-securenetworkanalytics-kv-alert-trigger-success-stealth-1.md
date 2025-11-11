# Code Changes for cisco-securenetworkanalytics-kv-alert-trigger-success-stealth-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_description', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_port', 'host', 'operation', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_name |  | ['Notification="+[^\|]+\|({alert_type}({alert_name}[^"\|]+))', 'signature="({alert_type}({alert_name}[^"]+))"'] |
| added_regex_field | alert_type |  | ['Notification="+[^\|]+\|({alert_type}({alert_name}[^"\|]+))', 'signature="({alert_type}({alert_name}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |