# Code Changes for microsoft-x-csv-email-deliver (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'host', 'num_recipients', 'orig_user', 'return_path', 'time'] |
| edit_regex_field | action |  | ['({alert_name}STOREDRIVER,({action}[^,]+)),', '({alert_type}STOREDRIVER,({action}[^,]+)),'] |
| edit_regex_field | email_address |  | [',\s*(?:\'|")?({email_address}({orig_user}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))[^,]*?\s*(?:\'|")?,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){9}Incoming,', ',\s*[\'"]*(|MicrosoftExchange.*?|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[\'"]*)(?<!local)(?<!loc)(?<!localdomain)(?<!internal)\s*,(?:[^,]*,){2}Incoming,'] |
| edit_regex_field | orig_user |  | [',\s*(?:\'|")?({email_address}({orig_user}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))[^,]*?\s*(?:\'|")?,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){9}Incoming,'] |
| added_regex_field | alert_type |  | ['({alert_type}STOREDRIVER,({action}[^,]+)),'] |
| removed_attribute | DupFields |  | N/A |