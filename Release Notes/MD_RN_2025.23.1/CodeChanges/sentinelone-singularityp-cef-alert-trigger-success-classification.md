# Code Changes for sentinelone-singularityp-cef-alert-trigger-success-classification (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_source', 'alert_type', 'bytes', 'category', 'domain', 'file_name', 'file_path', 'file_type', 'group_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host_type', 'incident_status', 'kill_status', 'last_loggedin_user', 'malware_file_name', 'mitigation_mode', 'os', 'process_name', 'quarantine_status', 'result', 'site_name', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_process_name', 'src_translated_ip', 'src_translated_port', 'time', 'user', 'verdict'] |
| edit_regex_field | file_name |  | ['"fileDisplayName":\s*"({process_name}({file_name}[^"]+))'] |
| added_regex_field | process_name |  | ['"fileDisplayName":\s*"({process_name}({file_name}[^"]+))'] |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'SentinelOne Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | Platform |  | ['MacOS', 'SentinelOne', 'Unix', 'Windows'] |