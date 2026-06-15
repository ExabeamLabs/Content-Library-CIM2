# Code Changes for pan-aperture-json-file-activitymonitoring (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\Wuser"?\s*(=|:)\s*"(Unknown|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |
| edit_regex_field | email_domain |  | ['\Wuser"?\s*(=|:)\s*"(Unknown|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |