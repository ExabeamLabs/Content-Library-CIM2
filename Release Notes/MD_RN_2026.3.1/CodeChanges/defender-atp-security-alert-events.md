# Code Changes for defender-atp-security-alert-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['"userAccount":\{[^\}]+?accountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'exa_regex="userAccount":\{[^\}]+?accountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |