# Code Changes for microsoft-x-csv-email-received (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_recipients', 'email_subject', 'host', 'num_recipients', 'orig_user', 'return_path', 'src_domain', 'time'] |
| edit_regex_field | src_domain |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Originating,', ',\s*(?:\'|")?(|MicrosoftExchange.*?|({orig_user}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Originating,'] |
| added_regex_field | orig_user |  | [',\s*(?:\'|")?(|MicrosoftExchange.*?|({orig_user}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({src_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(?:\'|")?)\s*,(?:(?:\s*\'+[^\']*\'+)\s*,|(?:\s*"+[^"]*"+)\s*,|[^",]+?,|\s*,){2}Originating,'] |
| removed_attribute | DupFields |  | N/A |