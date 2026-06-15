# Code Changes for zscaler-ia-csv-network-traffic-success-zscalerclientconnector (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){1}"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |
| edit_regex_field | email_domain |  | ['\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d"(("[^"]+")?,){1}"({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"'] |