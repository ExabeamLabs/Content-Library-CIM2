# Code Changes for microsoft-x-csv-email-receive-failed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | [',\s*(?:\'|")?({email_address}({orig_user}[^,;@]+@[^\.,"\']+\.[^;,"\']+))[^,]*?\s*(?:\'|")?,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){9}Incoming,', ',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?:\'|")?)\s*,(?:[^,]*,){2}Incoming,', ',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?:\'|")?)\s*,([^,]*,){2}Incoming,'] |
| edit_regex_field | orig_user |  | [',\s*(?:\'|")?({email_address}({orig_user}[^,;@]+@[^\.,"\']+\.[^;,"\']+))[^,]*?\s*(?:\'|")?,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){9}Incoming,'] |
| removed_attribute | DupFields |  | N/A |