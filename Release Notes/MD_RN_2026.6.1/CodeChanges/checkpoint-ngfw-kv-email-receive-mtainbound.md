# Code Changes for checkpoint-ngfw-kv-email-receive-mtainbound (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['\Wto:"({email_recipients}({dest_email_address}((?=.{1,64}\@)[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+)@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"'] |
| edit_regex_field | email_address |  | ['\Wfrom:"({email_address}((?=.{1,64}\@)[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+)@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"'] |
| edit_regex_field | email_recipients |  | ['\Wto:"({email_recipients}({dest_email_address}((?=.{1,64}\@)[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+)@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"'] |