# Code Changes for pan-ngfw-cef-alert-trigger-success-panos (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'dest_host', 'dest_interface', 'dest_ip', 'dest_network_zone', 'dest_port', 'dest_translated_ip', 'domain', 'host', 'malware_url', 'network_app', 'protocol', 'rule', 'serial_num', 'src_host', 'src_interface', 'src_ip', 'src_network_zone', 'src_port', 'src_translated_ip', 'threat_category', 'time', 'user'] |
| added_regex_field | alert_subject |  | ['\sPanOSThreatID="*({alert_subject}[^"=\(]+?)(\s*\([^\)]+?\)?)"*\s+\w+=', '\scat=({alert_subject}[^=]+)\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |