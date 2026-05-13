# Code Changes for microsoft-x-csv-email-receive-failed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_recipients', 'email_subject', 'failure_reason', 'host', 'num_recipients', 'orig_user', 'result', 'return_path', 'src_domain', 'time'] |
| edit_regex_field | email_address |  | [',\s*(?:\'|")?({email_address}({orig_user}[^,;@]+@[^\.,"\']+\.[^;,"\']+))[^,]*?\s*(?:\'|")?,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){9}Incoming,', ',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Incoming,'] |
| removed_regex_field | email_domain |  | [] |
| added_regex_field | src_domain |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Incoming,'] |