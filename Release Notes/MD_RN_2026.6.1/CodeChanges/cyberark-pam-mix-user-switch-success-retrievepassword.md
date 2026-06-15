# Code Changes for cyberark-pam-mix-user-switch-success-retrievepassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\sFile=(({domain}[^\\]+)\\)?[^\-]+\-({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=', 'usrName=(({domain}[^\\=]+)(\\)+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | email_address |  | ['usrName=(({domain}[^\\=]+)(\\)+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | email_domain |  | ['usrName=(({domain}[^\\=]+)(\\)+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | result_reason |  | ['\sReason=(|({result_reason}[\s\S]*?))\s*(ExtraDetails|PvwaDetails|\[ORIGINAL REASON:|\|SESSLOGS)'] |
| edit_regex_field | user |  | ['usrName=(({domain}[^\\=]+)(\\)+)?(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |