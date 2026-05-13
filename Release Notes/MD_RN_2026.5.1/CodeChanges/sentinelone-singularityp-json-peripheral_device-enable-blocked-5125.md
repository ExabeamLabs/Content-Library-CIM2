# Code Changes for sentinelone-singularityp-json-peripheral_device-enable-blocked-5125 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_json_path=$..creator,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$..creator,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | full_name |  | ['exa_json_path=$..creator,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | user |  | ['exa_json_path=$..creator,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?))|({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |