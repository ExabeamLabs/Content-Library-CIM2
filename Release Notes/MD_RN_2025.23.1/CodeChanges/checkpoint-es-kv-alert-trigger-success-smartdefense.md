# Code Changes for checkpoint-es-kv-alert-trigger-success-smartdefense (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Check Point Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address'])]), ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |