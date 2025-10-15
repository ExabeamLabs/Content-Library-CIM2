# Code Changes for salesforce-sf-cef-email-send-success-emailmessage (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['cc_address', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'orig_user', 'time'] |
| edit_regex_field | email_address |  | ['ValidatedFromAddress\\=({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)));'] |
| edit_regex_field | email_domain |  | ['ValidatedFromAddress\\=({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)));'] |
| added_regex_field | orig_user |  | ['ValidatedFromAddress\\=({orig_user}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)));'] |
| removed_attribute | DupFields |  | N/A |