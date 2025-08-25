# Code Changes for microsoft-mcas-json-alert-trigger-success-login (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'host', 'incident_status', 'result', 'src_ip', 'src_port', 'technique', 'time', 'user'] |
| added_regex_field | alert_id |  | ['"incidentId":"({alert_id}\d+)'] |
| added_regex_field | result |  | ['"evidence".+?"verdict":"({result}[^"]+)', 'exa_regex="evidence".+?"verdict":"({result}[^"]+)"'] |
| added_regex_field | technique |  | ['"mitreTechniques":\[({technique}[^\]]+)\]'] |