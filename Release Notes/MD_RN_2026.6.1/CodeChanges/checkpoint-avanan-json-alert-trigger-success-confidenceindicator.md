# Code Changes for checkpoint-avanan-json-alert-trigger-success-confidenceindicator (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.description,exa_regex=.+?\(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+?))\\'s mailbox\)'] |
| edit_regex_field | dest_email_domain |  | ['exa_json_path=$.description,exa_regex=.+?\(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+?))\\'s mailbox\)'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.senderAddress,exa_regex=^({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.senderAddress,exa_regex=^({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$'] |