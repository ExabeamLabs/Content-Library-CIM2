# Code Changes for checkpoint-ia-kv-vpn-login-success-successfullogin (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | full_name | ['(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] | ['(U|u)ser=(-|({full_name}[^\(\|]+)\s+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user | ['(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] | ['(U|u)ser=(-|({full_name}[^\(\|]+)\s+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_group_name | ['\|src_user_group=({user_group_name}.+?)\s*\|'] | ['\|src_user_group=({user_group_name}[^\|].*?)\s*\|'] |