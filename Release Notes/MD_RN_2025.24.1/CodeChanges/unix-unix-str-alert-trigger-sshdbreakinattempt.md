# Code Changes for unix-unix-str-alert-trigger-sshdbreakinattempt (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_type', 'host', 'process_id', 'process_name', 'src_host', 'src_ip', 'src_port'] |
| edit_regex_field | alert_name |  | ['({alert_type}({alert_name}POSSIBLE BREAK-IN ATTEMPT!))'] |
| added_regex_field | alert_type |  | ['({alert_type}({alert_name}POSSIBLE BREAK-IN ATTEMPT!))'] |
| removed_attribute | DupFields |  | N/A |