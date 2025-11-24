# Code Changes for snort-s-cef-alert-trigger-success-snort (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'host', 'protocol', 'src_ip', 'src_port'] |
| edit_regex_field | alert_name |  | ['CEF:([^\|]*\|){4}({alert_type}({alert_name}[^|]+))'] |
| added_regex_field | alert_type |  | ['CEF:([^\|]*\|){4}({alert_type}({alert_name}[^|]+))'] |
| removed_attribute | DupFields |  | N/A |