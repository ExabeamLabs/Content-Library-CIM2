# Code Changes for dropbox-d-cef-vpnfileapp-4 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['"participants":\[\{"\.tag":"user","user":\s*[^\}]*?"email":"(?:N\/A|({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |
| edit_regex_field | dest_email_domain |  | ['"participants":\[\{"\.tag":"user","user":\s*[^\}]*?"email":"(?:N\/A|({dest_email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |
| edit_regex_field | email_address |  | ['"actor":\s*[^\}]*?"email":\s*"(?:N\/A|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |
| edit_regex_field | email_domain |  | ['"actor":\s*[^\}]*?"email":\s*"(?:N\/A|({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"'] |