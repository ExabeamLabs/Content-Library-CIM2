# Code Changes for microsoft-o365-sk4-app-activity-success-setinboxrule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"UserId":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'UserId":"({email_address}[^"\\,]+@({email_domain}[^",]+))"'] |
| edit_regex_field | email_domain |  | ['"UserId":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'UserId":"({email_address}[^"\\,]+@({email_domain}[^",]+))"'] |
| edit_regex_field | user |  | ['"UserId":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'UserId":"(\\.+)?\/(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"\\=]+))(\\)?\\"\s*on behalf'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'email_rule-modify:success'] |