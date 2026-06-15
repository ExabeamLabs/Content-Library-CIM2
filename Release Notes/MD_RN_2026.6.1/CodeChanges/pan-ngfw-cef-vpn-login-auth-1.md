# Code Changes for pan-ngfw-cef-vpn-login-auth-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['PanOSSourceUserName=(({email_address}[^@=]+@[^\.=]+\.[^=]+)|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=', 'suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+='] |
| edit_regex_field | email_address |  | ['PanOSSourceUserName=(({email_address}[^@=]+@[^\.=]+\.[^=]+)|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=', 'suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+='] |
| edit_regex_field | email_domain |  | ['suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+='] |
| edit_regex_field | user |  | ['PanOSSourceUserName=(({email_address}[^@=]+@[^\.=]+\.[^=]+)|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+=', 'suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s\w+='] |