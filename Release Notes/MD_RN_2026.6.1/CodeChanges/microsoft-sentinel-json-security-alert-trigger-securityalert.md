# Code Changes for microsoft-sentinel-json-security-alert-trigger-securityalert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$.CompromisedEntity,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({src_host}[\w\-\.]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.CompromisedEntity,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({src_host}[\w\-\.]+))'] |
| edit_regex_field | src_host |  | ['exa_json_path=$.CompromisedEntity,exa_regex=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({src_host}[\w\-\.]+))'] |