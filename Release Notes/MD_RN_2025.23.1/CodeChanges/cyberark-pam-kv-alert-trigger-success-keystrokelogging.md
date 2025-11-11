# Code Changes for cyberark-pam-kv-alert-trigger-success-keystrokelogging (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_domain', 'alert_name', 'alert_severity', 'alert_type', 'app', 'dest_host', 'dest_ip', 'dest_port', 'dest_service_name', 'domain', 'event_code', 'host', 'malware_url', 'operation', 'safe_value', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | alert_name |  | [';Message="(|({alert_name}[^"]+?))\s*"'] |
| added_regex_field | alert_type |  | [';Message="(|({alert_type}[^"]+?))\s*"'] |
| removed_attribute | DupFields |  | N/A |