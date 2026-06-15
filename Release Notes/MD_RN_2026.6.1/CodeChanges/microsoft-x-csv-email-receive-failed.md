# Code Changes for microsoft-x-csv-email-receive-failed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['FAIL,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*)'] |
| edit_regex_field | dest_email_domain |  | ['FAIL,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*)'] |
| edit_regex_field | email_address |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Incoming,'] |
| edit_regex_field | email_recipients |  | ['FAIL,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*)'] |
| edit_regex_field | orig_user |  | ['FAIL,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({orig_user}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)'] |
| edit_regex_field | src_domain |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Incoming,'] |