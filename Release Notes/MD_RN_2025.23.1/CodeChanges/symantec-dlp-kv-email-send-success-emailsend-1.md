# Code Changes for symantec-dlp-kv-email-send-success-emailsend-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_email_address', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'file_name', 'host', 'protocol', 'target', 'time', 'user'] |
| edit_regex_field | email_domain |  | ['(?i)recipients="*(?=[\w.]+@[\w.])?({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)', '(?i)recipients="*(?=[\w.]+@[\w.])?({email_recipients}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)', '(?i)sender="*(?=[\w.]+@[\w.])({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)'] |
| added_regex_field | alert_type |  | ['(?i)policy="*({alert_type}[^",]+)("|,|\s*$)'] |
| added_regex_field | email_recipients |  | ['(?i)recipients="*(?=[\w.]+@[\w.])?({email_recipients}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))("|,|\s*$)'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'dlp'), ('NameTemplate', 'Vontu DLP Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'dest_address'), ('Fields', ['dest_ip->ip_address', 'dest_host->host_name'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |