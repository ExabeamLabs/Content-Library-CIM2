# Code Changes for netskope-sc-json-alert-trigger-success-compromised-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_email_address', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'host', 'malware_url', 'protocol', 'src_ip', 'src_port', 'time', 'user', 'user_agent', 'web_domain'] |
| added_regex_field | action |  | ['"action":\s*"({action}[^"]+)'] |