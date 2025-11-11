# Code Changes for microsoft-defenderep-sk4-alert-trigger-success-windowsdefenderav (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'host', 'incident_status', 'result', 'src_ip', 'src_port', 'technique', 'time'] |
| edit_regex_field | dest_host |  | ['"HostName":\s*"((?i)localhost|({host}({dest_host}[\w\-.]+)))'] |
| added_regex_field | host |  | ['"HostName":\s*"((?i)localhost|({host}({dest_host}[\w\-.]+)))'] |
| removed_attribute | DupFields |  | N/A |