# Code Changes for vmware-carbonblackappctrl-cef-alert-trigger-success-policy_enforce (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['duser=((NT AUTHORITY|({domain}[^\\=]+))\\+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)'] |
| edit_regex_field | email_address |  | ['duser=((NT AUTHORITY|({domain}[^\\=]+))\\+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)'] |
| edit_regex_field | user |  | ['duser=((NT AUTHORITY|({domain}[^\\=]+))\\+)?(SYSTEM|NETWORK SERVICE|LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)'] |