# Code Changes for sentinelone-singularityp-json-endpoint-logout-success-logins (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['"src.process.user":"((({domain}[^\\"]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..[\'src.process.user\'],exa_regex=^((({domain}[^\\"$]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))($|")'] |
| edit_regex_field | user |  | ['"event.login.userName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"src.process.user":"((({domain}[^\\"]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_json_path=$..[\'src.process.user\'],exa_regex=^((({domain}[^\\"$]+))\\+)?(({user}Système|LOCAL SERVICE|NETWORK SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))($|")', 'exa_regex="event.login.userName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |