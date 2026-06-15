# Code Changes for checkmarx-checkm-json-user-modify-success-userupdated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_name |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |
| edit_regex_field | dest_email_domain |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |
| edit_regex_field | dest_user |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |
| edit_regex_field | email_address |  | ['exa_json_path=$.UserName,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$.UserName,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))$'] |
| edit_regex_field | user |  | ['exa_json_path=$.UserName,exa_regex=^(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))$'] |