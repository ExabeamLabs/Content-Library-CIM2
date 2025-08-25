# Code Changes for microsoft-azureadip-json-alert-trigger-success-exfiltration (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | Product |  | Microsoft Purview |
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'domain', 'email_address', 'full_name', 'result', 'technique', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | alert_id |  | ['"id":\s*"({alert_id}[^"]+)"', '"incidentId":"({alert_id}\d+)'] |
| added_regex_field | result |  | ['"evidence".+?"verdict":"({result}[^"]+)', 'exa_regex="evidence".+?"verdict":"({result}[^"]+)"'] |
| added_regex_field | technique |  | ['"mitreTechniques":\[({technique}[^\]]+)\]'] |
| edit_attribute | legacy_activity_type |  | ['dlp-alert'] |
| edit_attribute | Platform |  | ['Microsoft Purview'] |