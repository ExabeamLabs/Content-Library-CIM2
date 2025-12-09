# Code Changes for fortinet-fortisiem-kv-alert-trigger-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'category', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'device_id', 'email_address', 'email_domain', 'event_category', 'event_name', 'host', 'malware_file_name', 'session_id', 'severity', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['\Wdevname="({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | alert_name |  | ['\Wmsg="({alert_name}[^"]+)'] |
| added_regex_field | alert_severity |  | ['\Wpri="({alert_severity}[^"]+)"'] |
| added_regex_field | alert_subject |  | ['\Wsubtype="({alert_subject}[^"]+)"'] |
| added_regex_field | alert_type |  | ['\Wtype=({alert_type}[^"]+)'] |
| added_regex_field | dest_host |  | ['\Wdevname="({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |