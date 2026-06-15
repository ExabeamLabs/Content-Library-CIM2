# Code Changes for pan-ngfw-cef-alert-trigger-success-panos-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['suser=((({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+\w+='] |
| edit_regex_field | email_address |  | ['suser=((({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+\w+='] |
| edit_regex_field | email_domain |  | ['suser=((({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+\w+='] |
| edit_regex_field | user |  | ['suser=((({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+\w+='] |