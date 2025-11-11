# Code Changes for pan-cortex-mix-alert-trigger-success-xdr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'dest_ip', 'dest_port', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_sha256', 'malware_url', 'process_command_line', 'process_name', 'process_path', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | alert_subject |  | ['CEF:[^|]+?\|([^\|]+\|){4}({alert_subject}[^\|]+)'] |
| removed_attribute | DupFields |  | N/A |