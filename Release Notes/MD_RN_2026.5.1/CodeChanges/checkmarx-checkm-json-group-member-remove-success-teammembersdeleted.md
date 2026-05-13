# Code Changes for checkmarx-checkm-json-group-member-remove-success-teammembersdeleted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_email_address', 'dest_email_domain', 'dest_user', 'dest_user_id', 'email_address', 'email_domain', 'group_id', 'group_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_email_address |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |
| edit_regex_field | dest_email_domain |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |
| edit_regex_field | dest_user |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |
| added_regex_field | account_name |  | ['exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}({account_name}[\w\.\-]{1,40}\$?)))\\?"'] |