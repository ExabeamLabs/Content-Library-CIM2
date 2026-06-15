# Code Changes for sentinelone-singularityp-json-endpoint-login-success-logins (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | email_address |  | ['exa_regex=userName":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"src.process.user":"((({domain}[^\\"]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..[\'src.process.user\'],exa_regex=^((({domain}[^\\"$]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))($|")', "exa_json_path=$.['event.login.userName'],exa_regex=^({user}[\w\.\-\!\#\^\~]{1,40}\$?)$", 'exa_regex=userName":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |