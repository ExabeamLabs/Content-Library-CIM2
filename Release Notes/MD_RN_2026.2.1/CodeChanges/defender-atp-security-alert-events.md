# Code Changes for defender-atp-security-alert-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'host', 'incident_status', 'more_info', 'result', 'src_ip', 'src_port', 'technique', 'time', 'user', 'workspace_name'] |
| added_regex_field | more_info |  | ['"incidentWebUrl":"({more_info}[^"]+)"'] |
| added_regex_field | workspace_name |  | ['"WorkspaceName":"({workspace_name}[^"]+)"'] |