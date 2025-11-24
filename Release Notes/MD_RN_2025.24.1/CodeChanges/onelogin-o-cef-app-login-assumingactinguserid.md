# Code Changes for onelogin-o-cef-app-login-assumingactinguserid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'activity_id', 'additional_info', 'app', 'dest_email_address', 'dest_email_domain', 'email_address', 'email_domain', 'failure_reason', 'full_name', 'operation', 'src_ip', 'src_port', 'time', 'user_id'] |
| edit_regex_field | email_address |  | ['suser=(({account}({user_id}\d+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | email_domain |  | ['suser=(({account}({user_id}\d+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| edit_regex_field | user_id |  | ['"user_id":({account}({user_id}\d+))', 'suser=(({account}({user_id}\d+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| added_regex_field | account |  | ['"user_id":({account}({user_id}\d+))', 'suser=(({account}({user_id}\d+))|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))'] |
| removed_attribute | DupFields |  | N/A |