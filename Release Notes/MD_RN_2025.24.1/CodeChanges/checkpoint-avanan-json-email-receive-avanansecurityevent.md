# Code Changes for checkpoint-avanan-json-email-receive-avanansecurityevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'category', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_attachments', 'email_domain', 'email_recipients', 'email_subject', 'file_name', 'full_name', 'orig_user', 'result', 'src_ip', 'time'] |
| edit_regex_field | email_address |  | ['from_email\\*":\\*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'from_email\\*":\\*"({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | email_domain |  | ['from_email\\*":\\*"({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'from_email\\*":\\*"({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| added_regex_field | orig_user |  | ['from_email\\*":\\*"({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| removed_attribute | DupFields |  | N/A |