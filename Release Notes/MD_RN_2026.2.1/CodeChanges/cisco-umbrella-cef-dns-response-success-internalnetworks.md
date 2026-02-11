# Code Changes for cisco-umbrella-cef-dns-response-success-internalnetworks (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"identities":\["({full_name}[^\("]+?)(?:\s*\(\w+}\)\s*)?(\s+\(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\))",("({host}[\w\-\.]+)")?'] |