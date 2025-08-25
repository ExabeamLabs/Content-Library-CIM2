# Code Changes for symantec-endpointprotection-kv-alert-trigger-success-symanteceprisk (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_type', 'dest_ip', 'dest_mac', 'dest_port', 'domain', 'event_name', 'host', 'local_host_ip', 'location', 'malware_url', 'occurrences', 'process_dir', 'process_name', 'process_path', 'protocol', 'src_host', 'src_mac', 'src_port', 'time', 'user'] |
| added_regex_field | action |  | ['Remote Host MAC:([^,]+,){3}({action}[^,]+)'] |
| added_regex_field | protocol |  | ['Remote Host MAC:([^,]+,){2}({protocol}[^,]+)'] |
| edit_attribute | legacy_activity_type |  | ['process-alert'] |