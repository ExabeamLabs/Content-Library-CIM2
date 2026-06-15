# Code Changes for microsoft-x-csv-email-send-failed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | [',\s*(?:\'|")?([^,]+(Recipients_cn)\=)?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*?)\s*(?:\'|")?,([^,]*,){9}Originating,'] |
| edit_regex_field | dest_email_domain |  | [',\s*(?:\'|")?([^,]+(Recipients_cn)\=)?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*?)\s*(?:\'|")?,([^,]*,){9}Originating,'] |
| edit_regex_field | email_address |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,([^,]*,){2}Originating,'] |
| edit_regex_field | email_domain |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,([^,]*,){2}Originating,', ',\s*(?:\'|")?(|MicrosoftExchange.*?|({orig_user}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,([^,]*,){2}Originating,'] |
| edit_regex_field | email_recipients |  | [',\s*(?:\'|")?([^,]+(Recipients_cn)\=)?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*?)\s*(?:\'|")?,([^,]*,){9}Originating,'] |
| edit_regex_field | orig_user |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({orig_user}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,([^,]*,){2}Originating,'] |