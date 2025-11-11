# Code Changes for symantec-dlp-cef-alert-trigger-success-symantecdlp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_subject', 'alert_type', 'domain', 'email_address', 'file_name', 'host', 'process_dir', 'protocol', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | alert_subject |  | ['\|Symantec\|DLP.*?\|([^|]*\|){2}({alert_subject}[^|]+)\|'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'dlp'), ('NameTemplate', 'Symantec DLP Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address', 'src_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |