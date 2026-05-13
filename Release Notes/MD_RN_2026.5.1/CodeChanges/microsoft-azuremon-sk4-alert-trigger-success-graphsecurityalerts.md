# Code Changes for microsoft-azuremon-sk4-alert-trigger-success-graphsecurityalerts (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'app', 'domain', 'email_address', 'tenant_id', 'time', 'user'] |
| edit_regex_field | domain |  | ['"accountName":"({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"domainName":"({domain}[^"]+)"', '"userPrincipalName":"(null|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | email_address |  | ['"userPrincipalName":"(null|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"accountName":"({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"userPrincipalName":"(null|({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | tenant_id |  | ['"azureTenantId":\s*"({tenant_id}[^"]+)"'] |