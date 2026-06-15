# Code Changes for mimecast-seg-cef-app-activity-success-messageviewlogs (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"to":"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({target}[^"]+)")'] |
| edit_regex_field | dest_email_domain |  | ['"to":"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({target}[^"]+)")'] |
| edit_regex_field | email_address |  | ['"from":"\s*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"', '"viewer":"\s*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"'] |
| edit_regex_field | email_domain |  | ['"from":"\s*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"', '"viewer":"\s*(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)))"'] |
| edit_regex_field | target |  | ['"to":"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({target}[^"]+)")'] |