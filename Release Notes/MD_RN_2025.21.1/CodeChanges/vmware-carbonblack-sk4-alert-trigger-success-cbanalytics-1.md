# Code Changes for vmware-carbonblack-sk4-alert-trigger-success-cbanalytics-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_reason', 'alert_severity', 'alert_type', 'domain', 'email_address', 'email_domain', 'host', 'os', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'primary_key', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'src_ip', 'src_port', 'threat_id', 'time', 'url', 'user'] |
| edit_regex_field | threat_id |  | ['"threat_id"+:"+({alert_id}({threat_id}[^"]+))"'] |
| added_regex_field | alert_id |  | ['"threat_id"+:"+({alert_id}({threat_id}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |