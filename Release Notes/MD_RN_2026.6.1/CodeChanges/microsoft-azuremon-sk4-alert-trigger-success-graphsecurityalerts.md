# Code Changes for microsoft-azuremon-sk4-alert-trigger-success-graphsecurityalerts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"accountName":"({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"domainName":"({domain}[^"]+)"', '"userPrincipalName":"(null|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | email_address |  | ['"userPrincipalName":"(null|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"accountName":"({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"userPrincipalName":"(null|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |