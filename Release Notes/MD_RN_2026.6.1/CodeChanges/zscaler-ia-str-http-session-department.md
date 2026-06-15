# Code Changes for zscaler-ia-str-http-session-department (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['\suser=(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s@]+)\s*(\w+=|$)', 'login=({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |