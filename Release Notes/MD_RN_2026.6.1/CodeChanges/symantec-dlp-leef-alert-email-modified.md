# Code Changes for symantec-dlp-leef-alert-email-modified (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\|usrName=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({email_address}[^\|@]+@[^\|@]+)|(N\/A|([^\\\|=]*\\)*({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '\|usrName=(?=[\w.]+@[\w.])({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['\|usrName=(?=[\w.]+@[\w.])({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |