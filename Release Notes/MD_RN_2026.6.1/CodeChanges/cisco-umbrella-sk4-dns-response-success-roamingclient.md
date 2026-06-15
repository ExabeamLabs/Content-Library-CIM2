# Code Changes for cisco-umbrella-sk4-dns-response-success-roamingclient (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['"identities":\["({full_name}[^\("]+?)(?:\s*\(\w+\)\s*)?(\s+\(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\))",("({host}[\w\-\.]+)")?'] |
| edit_regex_field | email_domain |  | ['"identities":\["({full_name}[^\("]+?)(?:\s*\(\w+\)\s*)?(\s+\(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\))",("({host}[\w\-\.]+)")?'] |
| edit_regex_field | full_name |  | ['"identities":\["({full_name}[^\("]+?)(?:\s*\(\w+\)\s*)?(\s+\(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\))",("({host}[\w\-\.]+)")?'] |
| edit_regex_field | host |  | ['"identities":\["({full_name}[^\("]+?)(?:\s*\(\w+\)\s*)?(\s+\(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\))",("({host}[\w\-\.]+)")?', '"identities":\[[^\]]*?"({host}[\w\-\.]+)"'] |