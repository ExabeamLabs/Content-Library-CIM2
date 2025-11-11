# Code Changes for juniper-ps-str-user-delete-fail-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_domain', 'dest_email_address', 'dest_email_domain', 'dest_user', 'domain', 'email_address', 'email_domain', 'host', 'realm', 'role', 'time', 'user'] |
| edit_regex_field | dest_domain |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | dest_email_address |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | dest_email_domain |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | dest_user |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| added_regex_field | account_name |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| removed_attribute | DupFields |  | N/A |