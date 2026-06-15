# Code Changes for sophos-xgfirewall-kv-network-traffic-success-firewallrule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\suser_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s'] |
| edit_regex_field | email_domain |  | ['\suser_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s'] |
| edit_regex_field | user |  | ['\suser_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s'] |