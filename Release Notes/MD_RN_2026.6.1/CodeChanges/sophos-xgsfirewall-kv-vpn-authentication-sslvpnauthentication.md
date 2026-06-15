# Code Changes for sophos-xgsfirewall-kv-vpn-authentication-sslvpnauthentication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['user_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s'] |
| edit_regex_field | email_domain |  | ['user_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s'] |
| edit_regex_field | user |  | ['user_name="(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s'] |