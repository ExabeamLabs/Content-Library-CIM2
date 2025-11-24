# Code Changes for bitdefender-gz-cef-alert-trigger-success-gravityzone (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'detection_level', 'domain', 'file_path', 'file_type', 'host', 'malware_url', 'method', 'operation', 'protocol', 'suid', 'time', 'url', 'user'] |
| edit_regex_field | alert_severity |  | ['BitdefenderGZDetectionLevel=({detection_level}({alert_severity}.*?))\s\w+='] |
| added_regex_field | detection_level |  | ['BitdefenderGZDetectionLevel=({detection_level}({alert_severity}.*?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |