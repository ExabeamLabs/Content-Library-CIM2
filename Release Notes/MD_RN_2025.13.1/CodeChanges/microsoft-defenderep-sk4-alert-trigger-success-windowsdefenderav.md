# Code Changes for microsoft-defenderep-sk4-alert-trigger-success-windowsdefenderav (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'incident_status', 'result', 'src_ip', 'src_port', 'technique', 'time'] |
| edit_regex_field | alert_id |  | ['"SystemAlertId"+:"+({alert_id}[^"]+)', '"incidentId":\s*"({alert_id}\d+)'] |
| added_regex_field | result |  | ['"evidence".+?"verdict":\s*"({result}[^"]+)'] |
| added_regex_field | technique |  | ['"mitreTechniques":\s*\[({technique}[^\]]+)\]'] |