# Code Changes for redshield-rswaf-kv-alert-trigger-success-asm (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'host', 'method', 'policy_name', 'protocol', 'result_code', 'src_ip', 'src_port', 'status_msg', 'time', 'uri', 'user'] |
| edit_regex_field | alert_name |  | [';TYPE=({alert_type}({alert_name}[^=;]+))'] |
| added_regex_field | alert_type |  | [';TYPE=({alert_type}({alert_name}[^=;]+))'] |
| removed_attribute | DupFields |  | N/A |