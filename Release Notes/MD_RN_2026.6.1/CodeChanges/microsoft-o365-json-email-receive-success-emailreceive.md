# Code Changes for microsoft-o365-json-email-receive-success-emailreceive (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.result.internal_recipients,exa_regex=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)'] |
| edit_regex_field | dest_email_domain |  | ['exa_json_path=$.result.internal_recipients,exa_regex=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.result.message,exa_regex= from (\'|)({email_address}[^"\s@]+@[^"\'\s@]+)', 'exa_json_path=$.result.message,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.result.message,exa_regex=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_recipients |  | ['exa_json_path=$.result.internal_recipients,exa_regex=({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^"]*)'] |