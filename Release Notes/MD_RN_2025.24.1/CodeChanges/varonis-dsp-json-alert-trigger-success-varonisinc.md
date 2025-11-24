# Code Changes for varonis-dsp-json-alert-trigger-success-varonisinc (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'first_name', 'full_name', 'host', 'last_name', 'result', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['\scs2=\s*(?:|({alert_type}({alert_name}.+?)))(\s+likely|\s+\w+=)'] |
| added_regex_field | alert_type |  | ['\scs2=\s*(?:|({alert_type}({alert_name}.+?)))(\s+likely|\s+\w+=)'] |
| removed_attribute | DupFields |  | N/A |