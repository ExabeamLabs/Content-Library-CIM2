# Code Changes for abnormalsecurity-as-json-alert-trigger-success-attacktype-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$..recipientAddress,exa_regex=({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$..toAddresses,exa_regex=^(|({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\"]*))$'] |
| edit_regex_field | dest_email_domain |  | ['exa_json_path=$..recipientAddress,exa_regex=({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$..toAddresses,exa_regex=^(|({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\"]*))$'] |
| edit_regex_field | email_address |  | ['exa_json_path=$..fromAddress,exa_regex=^(|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$..fromAddress,exa_regex=^(|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))$'] |
| edit_regex_field | email_recipients |  | ['exa_json_path=$..toAddresses,exa_regex=^(|({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\"]*))$'] |