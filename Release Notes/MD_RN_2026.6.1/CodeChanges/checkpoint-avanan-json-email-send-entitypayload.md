# Code Changes for checkpoint-avanan-json-email-send-entitypayload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.entityPayload.recipients,exa_regex=^\[?({email_recipients}"?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"?.*?)\s*\]?$'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.entityPayload.fromEmail,exa_regex=^({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.entityPayload.fromEmail,exa_regex=^({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$'] |
| edit_regex_field | email_recipients |  | ['exa_json_path=$.entityPayload.recipients,exa_regex=^\[?({email_recipients}"?({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"?.*?)\s*\]?$'] |