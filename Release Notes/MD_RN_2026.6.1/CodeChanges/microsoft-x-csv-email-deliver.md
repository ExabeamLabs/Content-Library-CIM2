# Code Changes for microsoft-x-csv-email-deliver (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'host', 'num_recipients', 'orig_user', 'return_path', 'time'] |
| edit_regex_field | dest_email_address |  | ['DELIVER,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*)'] |
| edit_regex_field | email_address |  | [',\s*[\'"]*(|MicrosoftExchange.*?|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[\'"]*)(?<!local)(?<!loc)(?<!localdomain)(?<!internal)\s*,(?:[^,]*,){2}Incoming,'] |
| edit_regex_field | email_domain |  | [',\s*[\'"]*(|MicrosoftExchange.*?|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[\'"]*)(?<!local)(?<!loc)(?<!localdomain)(?<!internal)\s*,(?:[^,]*,){2}Incoming,'] |
| edit_regex_field | email_recipients |  | ['DELIVER,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*)'] |
| edit_regex_field | orig_user |  | ['DELIVER,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({orig_user}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)'] |
| added_regex_field | dest_email_domain |  | ['DELIVER,(-,|"+(.+?)"+,|([^,]*),){2,3}\s*(?:\'|")?({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&\'+\/?=^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^,]*)'] |