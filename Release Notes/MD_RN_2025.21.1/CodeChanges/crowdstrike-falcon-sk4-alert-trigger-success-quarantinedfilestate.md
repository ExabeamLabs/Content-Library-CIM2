# Code Changes for crowdstrike-falcon-sk4-alert-trigger-success-quarantinedfilestate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'alert_name', 'alert_subject', 'alert_type', 'cid', 'file_dir', 'file_ext', 'file_name', 'file_path', 'new_hash', 'old_hash', 'os', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | alert_name |  | ['"event_simpleName":"({alert_subject}({alert_type}({alert_name}[^"]+)))'] |
| added_regex_field | alert_subject |  | ['"event_simpleName":"({alert_subject}({alert_type}({alert_name}[^"]+)))'] |
| added_regex_field | alert_type |  | ['"event_simpleName":"({alert_subject}({alert_type}({alert_name}[^"]+)))'] |
| removed_attribute | DupFields |  | N/A |