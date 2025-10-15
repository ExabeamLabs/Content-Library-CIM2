# Code Changes for crowdstrike-falcon-json-alert-trigger-success-dllinjection (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['aid', 'alert_id', 'alert_name', 'alert_subject', 'alert_type', 'cid', 'event_code', 'host', 'malware_file_name', 'os', 'time'] |
| edit_regex_field | alert_name |  | ['"event_simpleName":"({alert_subject}({event_code}({alert_type}({alert_name}[^"]+))))'] |
| added_regex_field | alert_subject |  | ['"event_simpleName":"({alert_subject}({event_code}({alert_type}({alert_name}[^"]+))))'] |
| added_regex_field | alert_type |  | ['"event_simpleName":"({alert_subject}({event_code}({alert_type}({alert_name}[^"]+))))'] |
| added_regex_field | event_code |  | ['"event_simpleName":"({alert_subject}({event_code}({alert_type}({alert_name}[^"]+))))'] |
| removed_attribute | DupFields |  | N/A |