# Code Changes for microsoft-evsecurity-kv-user-lock-success-4740-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'host', 'login_id', 'src_domain', 'src_host', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | login_id |  | ['Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$'] |
| edit_regex_field | src_domain |  | ['Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$'] |
| edit_regex_field | src_host |  | ['Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$'] |
| edit_regex_field | src_user |  | ['Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$'] |
| edit_regex_field | user |  | ['Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$'] |
| edit_regex_field | user_sid |  | ['Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$'] |
| added_regex_field | domain |  | ['Message=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({src_host}[^\s]+)\s({user_sid}[^\s]+)\s(.+?)\s({src_user}[^\s]+)\s({domain}({src_domain}[^\s]+))\s({login_id}[^\s]+)\s*$'] |
| removed_attribute | DupFields |  | N/A |