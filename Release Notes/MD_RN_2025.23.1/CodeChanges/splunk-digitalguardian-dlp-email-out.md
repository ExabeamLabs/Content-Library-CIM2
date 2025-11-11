# Code Changes for splunk-digitalguardian-dlp-email-out (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_email_address', 'dest_email_domain', 'domain', 'email_address', 'email_attachment', 'email_domain', 'email_recipients', 'email_subject', 'email_user', 'event_code', 'extension', 'file_name', 'host', 'time', 'user'] |
| edit_regex_field | email_address |  | ['Email_Address="(?:|({email_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))"', 'Email_Sender="(?:|({email_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))"'] |
| edit_regex_field | email_domain |  | ['Email_Address="(?:|({email_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))"', 'Email_Sender="(?:|({email_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))"'] |
| added_regex_field | email_user |  | ['Email_Address="(?:|({email_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))"', 'Email_Sender="(?:|({email_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))))"'] |
| removed_attribute | DupFields |  | N/A |