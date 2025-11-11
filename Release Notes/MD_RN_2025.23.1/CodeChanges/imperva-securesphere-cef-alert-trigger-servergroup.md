# Code Changes for imperva-securesphere-cef-alert-trigger-servergroup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'domain', 'server_group', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['CEF:([^\|]*\|){5}({alert_type}({alert_name}[^\|]+))'] |
| added_regex_field | alert_type |  | ['CEF:([^\|]*\|){5}({alert_type}({alert_name}[^\|]+))'] |
| removed_attribute | DupFields |  | N/A |