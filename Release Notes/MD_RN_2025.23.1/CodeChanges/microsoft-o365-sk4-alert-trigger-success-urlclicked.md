# Code Changes for microsoft-o365-sk4-alert-trigger-success-urlclicked (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_source', 'alert_subject', 'alert_type', 'email_address', 'email_domain', 'first_name', 'full_name', 'last_name', 'malware_url', 'src_ip', 'time', 'user', 'user_sid', 'user_type'] |
| edit_regex_field | alert_name |  | ['"Operation":"({alert_subject}({alert_name}[^"]+))'] |
| edit_regex_field | alert_type |  | ['"Workload":"({alert_source}({alert_type}[^"]+))'] |
| added_regex_field | alert_source |  | ['"Workload":"({alert_source}({alert_type}[^"]+))'] |
| added_regex_field | alert_subject |  | ['"Operation":"({alert_subject}({alert_name}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |