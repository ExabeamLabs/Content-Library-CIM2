# Code Changes for pan-ngfw-json-alert-trigger-success-spyware (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_subject', 'dest_ip', 'dest_port', 'device_name', 'email_address', 'file_name', 'host', 'src_ip', 'src_port', 'threat_category', 'user'] |
| edit_regex_field | alert_id |  | ['exa_json_path=$..ThreatID,exa_regex=({alert_subject}({alert_name}[^"\(]+?))\s*(\(({alert_id}[^"\)]\d+))'] |
| edit_regex_field | alert_name |  | ['exa_json_path=$..ThreatID,exa_regex=({alert_subject}({alert_name}[^"\(]+?))\s*(\(({alert_id}[^"\)]\d+))', 'exa_regex=({alert_subject}({alert_name}spyware))'] |
| added_regex_field | alert_subject |  | ['exa_json_path=$..ThreatID,exa_regex=({alert_subject}({alert_name}[^"\(]+?))\s*(\(({alert_id}[^"\)]\d+))', 'exa_regex=({alert_subject}({alert_name}spyware))'] |
| removed_attribute | DupFields |  | N/A |