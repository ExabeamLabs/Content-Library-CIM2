# Code Changes for cisco-fp-kv-alert-trigger-success-impactbits (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'generic'), ('NameTemplate', 'Cisco Firesight Alert ${alert_type} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address', 'dest_host->host_name'])])])]) |