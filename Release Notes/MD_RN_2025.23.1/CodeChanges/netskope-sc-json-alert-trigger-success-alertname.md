# Code Changes for netskope-sc-json-alert-trigger-success-alertname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'app', 'browser', 'bytes', 'category', 'dest_country', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'file_type', 'hash_md5', 'host', 'operation', 'os', 'os_version', 'policy_name', 'protocol', 'src_country', 'src_ip', 'src_port', 'time', 'user_agent', 'web_domain'] |
| edit_regex_field | alert_name |  | ['"alert_name":\s*"({alert_subject}({alert_name}[^",]+))'] |
| added_regex_field | alert_subject |  | ['"alert_name":\s*"({alert_subject}({alert_name}[^",]+))'] |
| removed_attribute | DupFields |  | N/A |