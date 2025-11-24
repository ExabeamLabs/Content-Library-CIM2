# Code Changes for claroty-ctd-cef-alert-trigger-success-newconflictasset (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_mac', 'dest_port', 'device_id', 'event_name', 'mitre_labels', 'protocol', 'severity', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'url'] |
| added_regex_field | alert_name |  | ['\|Schneider\|CTD\|([^\|]+\|){2}({alert_type}({alert_name}[^\|]+))\|'] |
| added_regex_field | alert_severity |  | ['CtdAlertScore=({alert_severity}\d+)', 'CtdSignatureCriticality=({alert_severity}[^=]+)\s+\w+='] |
| added_regex_field | alert_type |  | ['\|Schneider\|CTD\|([^\|]+\|){2}({alert_type}({alert_name}[^\|]+))\|'] |
| removed_attribute | DupFields |  | N/A |