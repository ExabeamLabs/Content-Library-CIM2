# Code Changes for salesforce-sf-sk4-app-activity-success-userlockedout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['suser=([^\s\\\=]+\\\=)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))'] |
| edit_regex_field | email_domain |  | ['suser=([^\s\\\=]+\\\=)?({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))'] |