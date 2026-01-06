# Code Changes for mimecast-seg-json-email-eventtype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.recipient,exa_regex=({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)', 'exa_json_path=$.recipients,exa_regex=({email_recipients}(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+),?)?[^"]*)'] |
| edit_regex_field | email_recipients |  | ['exa_json_path=$.recipients,exa_regex=({email_recipients}(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+),?)?[^"]*)'] |