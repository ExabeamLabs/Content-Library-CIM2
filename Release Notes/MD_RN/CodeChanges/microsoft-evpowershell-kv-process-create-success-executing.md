# Code Changes for microsoft-evpowershell-kv-process-create-success-executing (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain | ['"domain":"({domain}[^"]+)"', 'Context[^\]]+?User\s*\\?=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*'] | ['"domain":"({domain}[^"]+)"', 'Context[^\]]+?User\s*\\?=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*', '\sUser = (({domain}[^=]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\\s){0,5}\s{1,100}Connected User ='] |
| edit_regex_field | user | ['Context[^\]]+?User\s*\\?=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*'] | ['Context[^\]]+?User\s*\\?=\s*(({domain}[^=]+?)[\\\/]+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*', '\sUser = (({domain}[^=]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\t|\\r|\\n|\\s){0,5}\s{1,100}Connected User ='] |