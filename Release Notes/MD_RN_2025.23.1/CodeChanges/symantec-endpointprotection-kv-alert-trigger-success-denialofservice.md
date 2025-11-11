# Code Changes for symantec-endpointprotection-kv-alert-trigger-success-denialofservice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_name', 'alert_type', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'host', 'protocol', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | alert_type |  | ['SymantecServer:\s*.*?({alert_type}Denial of Service[^:]+?)\s*Description:'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'generic'), ('NameTemplate', 'Symantec Network Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address', 'dest_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |