# Code Changes for zyxel-usgflex-kv-alert-trigger-success-ips (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'category', 'dest_ip', 'dest_port', 'devid', 'email_address', 'email_domain', 'event_name', 'host', 'operation', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | alert_subject |  | ['\smsg="({alert_subject}[^"]+)'] |
| added_regex_field | alert_type |  | ['\scat="({alert_type}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |