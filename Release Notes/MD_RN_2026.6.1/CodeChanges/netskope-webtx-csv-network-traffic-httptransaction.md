# Code Changes for netskope-webtx-csv-network-traffic-httptransaction (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['^(-,|"+(.+?)"+,|([^,]*),){4}(-|(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({domain}[\w\-.]+))'] |
| edit_regex_field | email_address |  | [',(-|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),(-|({http_response_code}\d+))'] |
| edit_regex_field | http_response_code |  | [',(-|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),(-|({http_response_code}\d+))', ',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){3}(-|({http_response_code}\d+))'] |
| edit_regex_field | user |  | [',(-|(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),(-|({http_response_code}\d+))'] |
| edit_regex_field | web_domain |  | [',(\d\d\d\d-\d\d-\d\d),(-|\d+),(-,|"+(.+?)"+,|([^,]*),){63}(-|[^\/,]+\/+({web_domain}[\w\-.]+))'] |