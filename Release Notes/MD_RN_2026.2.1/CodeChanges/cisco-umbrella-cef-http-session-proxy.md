# Code Changes for cisco-umbrella-cef-http-session-proxy (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['"identities"+:\["+({dest_host}[\w-]+)\.?".*?"identityType":[^":]*?"(Anyconnect Roaming Client|Roaming Computers)"', '"identities":\[("({dest_host}[\w\-\.]+)")?,"({full_name}[^\("]+?)(?:\s*\(\w+}\)\s*)?(\s+\(({email_address}(([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9])+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\))"'] |