# Code Changes for symantec-dlp-kv-peripheral-storage-insert-success-devicewas (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'generic'), ('NameTemplate', 'Symantec ${device_class} insert found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_host->host_name', 'dest_ip->ip_address'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |