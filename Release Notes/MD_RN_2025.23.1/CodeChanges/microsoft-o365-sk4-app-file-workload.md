# Code Changes for microsoft-o365-sk4-app-file-workload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_severity', 'app', 'bytes', 'correlation_id', 'dest_email_address', 'dest_email_domain', 'dest_process_path', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'encrypted', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_sha1', 'hash_sha256', 'host', 'label_id', 'member', 'new_value', 'object', 'object_id', 'old_sensitivity_label', 'operation', 'os', 'resource', 'result', 'sensitivity_label', 'src_ip', 'src_port', 'target', 'time', 'url', 'user', 'user_agent', 'user_type', 'user_upn'] |
| edit_regex_field | operation |  | ['"Operation\\*"+:[\s\\]*"+({alert_name}({operation}[^"\\\.]*))'] |
| added_regex_field | alert_name |  | ['"Operation\\*"+:[\s\\]*"+({alert_name}({operation}[^"\\\.]*))'] |
| added_regex_field | bytes |  | ['"FileSize":\s*({bytes}\d+)'] |
| added_regex_field | hash_sha1 |  | ['"Sha1":\s*"({hash_sha1}[^"]+)"'] |
| added_regex_field | hash_sha256 |  | ['"Sha256":\s*"({hash_sha256}[^"]+)"'] |
| removed_attribute | DupFields |  | N/A |