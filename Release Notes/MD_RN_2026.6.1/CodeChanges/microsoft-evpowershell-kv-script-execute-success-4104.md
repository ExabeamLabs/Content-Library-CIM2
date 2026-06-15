# Code Changes for microsoft-evpowershell-kv-script-execute-success-4104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['AccountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', 'Microsoft-Windows-PowerShell\s+(NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+User', 'User(:|=)\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\w+?(:|=)', 'username=\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_upn |  | ['username=\s*(({user_upn}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |