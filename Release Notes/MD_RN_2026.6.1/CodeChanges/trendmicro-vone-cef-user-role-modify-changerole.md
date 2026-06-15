# Code Changes for trendmicro-vone-cef-user-role-modify-changerole (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\'User account\':\s*\'(({full_name}[^\'\s]+\s+[^\s\']+)|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |
| edit_regex_field | email_domain |  | ['\'User account\':\s*\'(({full_name}[^\'\s]+\s+[^\s\']+)|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |
| edit_regex_field | full_name |  | [' cs1=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^=]+?))((\s+\w+=)|\s*$)', '\'User account\':\s*\'(({full_name}[^\'\s]+\s+[^\s\']+)|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |
| edit_regex_field | user |  | [' cs1=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^=]+?))((\s+\w+=)|\s*$)', '\'User account\':\s*\'(({full_name}[^\'\s]+\s+[^\s\']+)|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\''] |