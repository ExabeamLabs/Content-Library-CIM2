# Code Changes for symantec-dlp-str-email-send-success-emailsend (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'dlp'), ('NameTemplate', 'Vontu DLP Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address', 'dest_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |