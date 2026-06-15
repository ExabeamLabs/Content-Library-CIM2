# Code Changes for microsoft-adfs-str-app-authentication-fail-411 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['Error message:\s*({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\s*\-\s*({failure_reason}.+?)\s+Exception details:'] |
| edit_regex_field | email_domain |  | ['Error message:\s*({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\s*\-\s*({failure_reason}.+?)\s+Exception details:'] |
| edit_regex_field | failure_reason |  | ['Error message:\s*({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\s*\-\s*({failure_reason}.+?)\s+Exception details:'] |