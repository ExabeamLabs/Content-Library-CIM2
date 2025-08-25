# Code Changes for microsoft-mcas-json-alert-trigger-success-alertanubisdetectionrepeatedactivitydelete (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'full_name', 'incident_status', 'location', 'result', 'src_host', 'src_ip', 'src_port', 'technique', 'time', 'user', 'user_upn'] |
| edit_regex_field | alert_id |  | ['"id":\s*"({alert_id}[^"]+)"', '"incidentId":\s*"({alert_id}\d+)'] |
| added_regex_field | result |  | ['"evidence".+?"verdict":"({result}[^"]+)', 'exa_regex="evidence".+?"verdict":"({result}[^"]+)"'] |
| added_regex_field | technique |  | ['"mitreTechniques":\[({technique}[^\]]+)\]'] |