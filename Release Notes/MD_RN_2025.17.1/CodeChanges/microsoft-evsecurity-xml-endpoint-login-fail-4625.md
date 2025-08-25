# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-4625 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*(?=\w)(({email_address}([A-Za-z0-9]+(?!\/)[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"<\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@<=]+))?)\s*<\/Data>'] |
| edit_regex_field | email_address |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*(?=\w)(({email_address}([A-Za-z0-9]+(?!\/)[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"<\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@<=]+))?)\s*<\/Data>'] |
| edit_regex_field | email_domain |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*(?=\w)(({email_address}([A-Za-z0-9]+(?!\/)[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"<\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@<=]+))?)\s*<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>\s*(?=\w)(({email_address}([A-Za-z0-9]+(?!\/)[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"<\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@<=]+))?)\s*<\/Data>', 'Logon Failed(:|=).+?Account Name(:|=)\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[\s;]*Account Domain(:|=)'] |