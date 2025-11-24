# Code Changes for eset-es-leef-alert-trigger-success-firewallevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category', 'dest_ip', 'dest_port', 'direction', 'domain', 'event_name', 'hash_sha256', 'host', 'operation', 'process_dir', 'process_name', 'process_path', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'url', 'user'] |
| added_regex_field | alert_type |  | ['\|ESET\|(?:[^\|]+\|){2}({alert_type}[^\|]+)'] |
| removed_attribute | DupFields |  | N/A |