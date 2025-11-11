# Code Changes for cisco-secureendpoint-sk4-alert-trigger-success-majorfaultraised (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'category', 'connector_guid', 'dest_ip', 'dest_port', 'domain', 'email_address', 'file_name', 'file_path', 'hash_md5', 'hash_sha1', 'hash_sha256', 'malware_url', 'process_path', 'product_name', 'result', 'src_host', 'src_ip', 'src_mac', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_type |  | ['event_type":\s*"({category}({alert_type}[^"]+))'] |
| edit_regex_field | file_path |  | ['file_path":\s*"(\\+\?\\+)?({malware_url}({file_path}[^"]+))'] |
| added_regex_field | category |  | ['event_type":\s*"({category}({alert_type}[^"]+))'] |
| added_regex_field | malware_url |  | ['file_path":\s*"(\\+\?\\+)?({malware_url}({file_path}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Cisco AMP Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])]), ConfigTree([('EntityType', 'file'), ('Name', 'file_name'), ('Fields', ['file_name->file_name'])])])]) |