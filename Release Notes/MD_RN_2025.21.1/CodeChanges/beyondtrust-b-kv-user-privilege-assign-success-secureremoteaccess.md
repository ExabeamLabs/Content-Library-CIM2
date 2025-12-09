# Code Changes for beyondtrust-b-kv-user-privilege-assign-success-secureremoteaccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'additional_info', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'email_address', 'email_domain', 'event_name', 'full_name', 'host', 'os', 'session_id', 'src_host', 'src_ip', 'src_port', 'src_user'] |
| edit_regex_field | dest_email_address |  | ['dstUser=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | dest_email_domain |  | ['dstUser=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | dest_user |  | ['dstUser=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | account |  | ['dstUser=(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |