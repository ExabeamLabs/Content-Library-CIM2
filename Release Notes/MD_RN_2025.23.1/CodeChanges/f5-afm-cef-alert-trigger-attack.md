# Code Changes for f5-afm-cef-alert-trigger-attack (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'attack_id', 'dest_ip', 'dest_port', 'host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_name |  | ['CEF:[^|]+\|([^|]+\|){4}(\/[^|]+|({alert_type}({alert_name}[^|]+)))', 'CEF:[^|]+\|([^|]+\|){4}({alert_type}({alert_name}\/[^=]+))\/'] |
| added_regex_field | alert_type |  | ['CEF:[^|]+\|([^|]+\|){4}(\/[^|]+|({alert_type}({alert_name}[^|]+)))', 'CEF:[^|]+\|([^|]+\|){4}({alert_type}({alert_name}\/[^=]+))\/'] |
| removed_attribute | DupFields |  | N/A |