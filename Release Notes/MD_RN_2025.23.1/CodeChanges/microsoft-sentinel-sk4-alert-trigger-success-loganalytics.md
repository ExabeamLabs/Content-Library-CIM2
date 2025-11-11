# Code Changes for microsoft-sentinel-sk4-alert-trigger-success-loganalytics (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'malware'), ('NameTemplate', 'Microsoft azure security Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |