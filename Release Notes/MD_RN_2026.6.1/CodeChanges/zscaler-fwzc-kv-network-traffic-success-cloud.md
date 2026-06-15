# Code Changes for zscaler-fwzc-kv-network-traffic-success-cloud (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\|user=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^@\"\|]+)@)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^\"@\|]+))\|'] |
| edit_regex_field | email_address |  | ['\|user=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^@\"\|]+)@)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^\"@\|]+))\|'] |
| edit_regex_field | email_domain |  | ['\|user=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^@\"\|]+)@)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^\"@\|]+))\|'] |
| edit_regex_field | full_name |  | ['\|user=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^@\"\|]+)@)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^\"@\|]+))\|'] |
| edit_regex_field | user |  | ['\|user=((\w+_)[^"\|]+|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '\|user=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|((({domain}[^@\"\|]+)@)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^\"@\|]+))\|'] |