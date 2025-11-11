# Code Changes for microsoft-evsecurity-kv-endpoint-login-fail-411-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['<UserId>(({domain}[^<\\]+)\\+)?(N\/A|({user}[\w\.\-\!\#\^\~]{1,40}\$?))</UserId>', '\sUser=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |