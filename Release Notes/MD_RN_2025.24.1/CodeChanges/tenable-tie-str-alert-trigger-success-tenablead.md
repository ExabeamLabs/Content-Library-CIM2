# Code Changes for tenable-tie-str-alert-trigger-success-tenablead (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'domain', 'event_code', 'full_name', 'group_name', 'host', 'object_dn', 'os', 'os_version', 'process_id', 'result_reason', 'time', 'user', 'user_sid', 'users'] |
| edit_regex_field | alert_subject |  | ['Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){9}"({result_reason}({alert_subject}[^"]+))'] |
| added_regex_field | result_reason |  | ['Tenable\.ad\s*\[\S+\]:\s("[^"]*"\s){9}"({result_reason}({alert_subject}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |