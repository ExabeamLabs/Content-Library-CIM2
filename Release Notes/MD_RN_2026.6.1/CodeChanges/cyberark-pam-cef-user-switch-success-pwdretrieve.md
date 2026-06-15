# Code Changes for cyberark-pam-cef-user-switch-success-pwdretrieve (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_domain |  | ['\sduser=(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({dest_domain}[^\\=]+?)(\\)+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | dest_email_address |  | ['\sduser=(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({dest_domain}[^\\=]+?)(\\)+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | dest_user |  | ['\sduser=(({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({dest_domain}[^\\=]+?)(\\)+)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | domain |  | ['\ssuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | email_address |  | ['\ssuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | user |  | ['\ssuser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\=]+?)(\\)+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |