# Code Changes for microsoft-o365-sk4-app-activity-success-sentmailbox (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"UserId":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\\"]+)\\+)(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({=user}[\w\.\-"]+)(@({=domain}[^"]+))?)'] |
| edit_regex_field | email_address |  | ['"UserId":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\\"]+)\\+)(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({=user}[\w\.\-"]+)(@({=domain}[^"]+))?)'] |
| edit_regex_field | email_domain |  | ['"UserId":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\\"]+)\\+)(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({=user}[\w\.\-"]+)(@({=domain}[^"]+))?)'] |
| edit_regex_field | user |  | ['"UserId":"(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(({domain}[^\\"]+)\\+)(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({=user}[\w\.\-"]+)(@({=domain}[^"]+))?)'] |
| edit_attribute | activity_type |  | ['mailbox-modify:success'] |