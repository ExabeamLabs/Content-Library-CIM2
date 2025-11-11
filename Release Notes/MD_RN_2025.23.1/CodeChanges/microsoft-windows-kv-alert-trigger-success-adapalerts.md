# Code Changes for microsoft-windows-kv-alert-trigger-success-adapalerts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'email_address', 'host', 'src_host', 'time', 'user'] |
| edit_regex_field | alert_type |  | ['\WALERT_PROFILE\s*=\s*({alert_name}({alert_type}[^=]+?))\s*(\]|([\w_]+)\s*=)'] |
| added_regex_field | alert_name |  | ['\WALERT_PROFILE\s*=\s*({alert_name}({alert_type}[^=]+?))\s*(\]|([\w_]+)\s*=)'] |
| removed_attribute | DupFields |  | N/A |