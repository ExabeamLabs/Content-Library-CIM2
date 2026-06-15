# Code Changes for juniper-ps-str-user-delete-fail-firewall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account_name |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | dest_domain |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | dest_email_address |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | dest_email_domain |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | dest_user |  | ['Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))'] |
| edit_regex_field | domain |  | ['\suser=(\\+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_address |  | ['\suser=(\\+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)'] |
| edit_regex_field | email_domain |  | ['\suser=(\\+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)'] |
| edit_regex_field | user |  | ['\suser=(\\+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)'] |