# Code Changes for microsoft-defenderep-json-alert-trigger-success-lateralmovement (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'full_name', 'incident_status', 'malware_family', 'more_info', 'process_id', 'process_name', 'result', 'src_host', 'src_ip', 'src_port', 'technique', 'time', 'user', 'user_upn', 'workspace_name'] |
| added_regex_field | more_info |  | ['"incidentWebUrl":"({more_info}[^"]+)"'] |
| added_regex_field | workspace_name |  | ['"WorkspaceName":"({workspace_name}[^"]+)"'] |