# Code Changes for vmware-airwatch-kv-endpoint-login-success-adminuserloggedin (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*Event Source:'] |
| edit_regex_field | email_address |  | ['User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*Event Source:'] |
| edit_regex_field | user |  | ['User:\s*((({domain}[^\\]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*Event Source:'] |