# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-4625-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['\s*Logon Failed(:|=).+?Account Name(:|=)\s*(({user_upn}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc))|(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({=domain}[^\s]+))?))\s*Account Domain:', '\s*Logon Failed(:|=).+?Account Name(:|=)\s*(\\r|\\t|\\n)*(-|({user}LOCAL SERVICE|SYSTEM|Administrator|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))[\s;]*(\\r|\\t|\\n)*Account Domain(:|=)'] |