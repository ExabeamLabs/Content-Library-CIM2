# Code Changes for netskope-sc-cef-alert-trigger-success-useralert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"user":\s*"(unknown|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({domain}[^"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"'] |
| edit_regex_field | email_address |  | ['"user":\s*"(unknown|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({domain}[^"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"'] |
| edit_regex_field | user |  | ['"user":\s*"(unknown|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({domain}[^"@\\\/]+)[\\\/]+)?(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))))"'] |