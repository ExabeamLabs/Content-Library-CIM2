# Code Changes for netskope-sc-sk4-alert-trigger-success-alertypedlp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_type', 'app', 'auth_method', 'browser', 'bytes', 'dest_ip', 'dest_port', 'domain', 'email_address', 'file_name', 'file_type', 'from_user_at', 'hash_md5', 'hash_sha256_at', 'host', 'location', 'malware_url', 'object', 'operation', 'os', 'protocol', 'referrer', 'rule', 'rule_count', 'shared_with_at', 'site_at', 'src_host', 'src_ip', 'src_port', 'threat_category', 'time', 'url', 'user', 'web_domain'] |
| edit_regex_field | alert_type |  | ['"activity":\s*"({alert_type}({operation}[^\"]+))', '"alert_type":"({alert_type}[^"]+)'] |
| edit_regex_field | object |  | ['"object":\s*"(\s+\"|(\s*(Unknown Unknown|unknown|Unknown|null|({file_name}({object}[^\"]+?)))\s*\"))'] |
| edit_regex_field | operation |  | ['"activity":\s*"({alert_type}({operation}[^\"]+))'] |
| edit_regex_field | src_host |  | ['"*hostname"*:"*({src_host}[^"]+)"', '"hostname":"({src_host}[^",]+)"'] |
| added_regex_field | file_name |  | ['"object":\s*"(\s+\"|(\s*(Unknown Unknown|unknown|Unknown|null|({file_name}({object}[^\"]+?)))\s*\"))'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Netskope Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |