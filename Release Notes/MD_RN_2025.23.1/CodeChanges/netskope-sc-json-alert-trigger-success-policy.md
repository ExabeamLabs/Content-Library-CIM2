# Code Changes for netskope-sc-json-alert-trigger-success-policy (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Netskope Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |