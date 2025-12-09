# Code Changes for proofpoint-tap-kv-email-receive-mailreceived (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'malware_score', 'phishing_score', 'result', 'spam_score', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_email_address |  | ['\srecipient="*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | dest_email_domain |  | ['\srecipient="*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| added_regex_field | email_recipients |  | ['\srecipient="*({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| removed_attribute | DupFields |  | N/A |