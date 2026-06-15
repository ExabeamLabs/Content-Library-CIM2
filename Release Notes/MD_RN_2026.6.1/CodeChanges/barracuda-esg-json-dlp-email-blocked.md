# Code Changes for barracuda-esg-json-dlp-email-blocked (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"email":"({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', '"hdr_to":"({email_recipients}(({dest_email_address}[^@,"]+@[^,"]+?),)?[^"]+?)",'] |
| edit_regex_field | dest_email_domain |  | ['"email":"({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |