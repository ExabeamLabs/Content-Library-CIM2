# Code Changes for vmware-carbonblackappctrl-kv-alert-trigger-success-execution-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'domain', 'file_ext', 'file_name', 'file_path', 'host', 'policy_name', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | alert_type |  | ['\ssubtype="({access}({alert_type}[^"]+))"'] |
| added_regex_field | access |  | ['\ssubtype="({access}({alert_type}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |