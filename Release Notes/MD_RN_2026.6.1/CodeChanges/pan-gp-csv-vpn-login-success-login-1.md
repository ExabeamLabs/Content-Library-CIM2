# Code Changes for pan-gp-csv-vpn-login-success-login-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | [',USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),'] |
| edit_regex_field | email_address |  | [',USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),'] |
| edit_regex_field | full_name |  | [',USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),'] |
| edit_regex_field | src_ip |  | [',USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),'] |
| edit_regex_field | user |  | [',USERID,login,.+?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^,]+)),'] |