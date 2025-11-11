# Code Changes for netskope-sc-sk4-alert-trigger-success-netskope (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_type', 'bytes', 'domain', 'email_address', 'file_ext', 'file_name', 'file_path_at', 'hash_md5', 'malware_file_name', 'malware_url', 'object', 'operation', 'policy_name', 'process_path', 'shared_with_at', 'site_at', 'time', 'url', 'user', 'user_ou'] |
| added_regex_field | file_path_at |  | ['"file_path":"({file_path_at}[^"]+)'] |
| added_regex_field | url |  | ['"url":"({url}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |