# Code Changes for fortinet-fortigate-kv-app-activity-system (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['\suser="(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(ANONYMOUS|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\@({domain}[^"]+))?))"'] |
| edit_regex_field | email_address |  | ['\suser="(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(ANONYMOUS|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\@({domain}[^"]+))?))"'] |
| edit_regex_field | user |  | ['\suser="(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(ANONYMOUS|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\@({domain}[^"]+))?))"'] |