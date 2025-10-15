# Code Changes for symantec-endpointprotection-kv-alert-trigger-success-symanteceprisk (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_mac', 'dest_port', 'domain', 'event_name', 'host', 'local_host_ip', 'location', 'malware_url', 'occurrences', 'priority', 'process_dir', 'process_name', 'process_path', 'protocol', 'src_host', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | time |  | ['(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)\s', 'Begin:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)'] |
| added_regex_field | alert_severity |  | ['(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)\s'] |
| added_regex_field | priority |  | ['(<({alert_severity}({priority}\d+))>)?({time}\w+\s\d+\s\d+:\d+:\d+)\s'] |