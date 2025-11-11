# Code Changes for symantec-endpointprotection-cef-alert-trigger-success-intrusiondetected (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_ip', 'dest_port', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'malware_file_name', 'malware_url', 'process_name', 'protection_name', 'result', 'scan_type', 'secondary_action', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_severity |  | ['\|Symantec\|Endpoint Protection\|([^|]*?\|){2}({alert_type}[^|(]+?)\s*(\([^|]*?)?\|(Unknown|({alert_severity}[^|]+))\|', '\|Symantec\|Endpoint Protection\|([^|]*?\|){2}({protection_name}[^|(]+?)\s*(\([^|]*?)?\|(Unknown|({alert_severity}[^|]+))\|'] |
| added_regex_field | protection_name |  | ['\|Symantec\|Endpoint Protection\|([^|]*?\|){2}({protection_name}[^|(]+?)\s*(\([^|]*?)?\|(Unknown|({alert_severity}[^|]+))\|'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Symantec Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |