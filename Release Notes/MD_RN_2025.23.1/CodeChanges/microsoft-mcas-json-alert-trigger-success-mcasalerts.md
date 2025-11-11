# Code Changes for microsoft-mcas-json-alert-trigger-success-mcasalerts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_type', 'app', 'country_code', 'domain', 'email_address', 'malware_url', 'original_risk_score', 'src_ip', 'src_port', 'time', 'user', 'user_uid'] |
| edit_regex_field | app |  | ['\srequestClientApplication=({alert_source}({app}[^=]+?))\s+\w+='] |
| added_regex_field | alert_source |  | ['\srequestClientApplication=({alert_source}({app}[^=]+?))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |