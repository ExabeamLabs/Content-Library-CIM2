# Code Changes for exabeam-phishingdetection-json-email-receive-success-phish (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_email_address', 'email_address', 'full_name', 'reporter', 'src_ip'] |
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.recipient,exa_regex=\<({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+)'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.sender,exa_regex=\<?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+)'] |
| added_regex_field | reporter |  | ['exa_json_path=$.reporter,exa_regex=\<?({reporter}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|\>]+)'] |