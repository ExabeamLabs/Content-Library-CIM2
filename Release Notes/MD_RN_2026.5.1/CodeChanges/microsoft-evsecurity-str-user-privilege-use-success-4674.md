# Code Changes for microsoft-evsecurity-str-user-privilege-use-success-4674 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['({dest_host}({host}[\w.\-]+))[,\]]\s*特権のあるオブジェクトで操作が試行されました。'] |
| edit_regex_field | domain |  | ['\sID:\s*({login_id}[^\s]+?)\s+アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン', 'アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン\s*ID:\s*({login_id}[^\s]+?)\s+オブジェクト:'] |
| edit_regex_field | event_code |  | ['({event_code}4674)'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w.\-]+))[,\]]\s*特権のあるオブジェクトで操作が試行されました。'] |
| edit_regex_field | login_id |  | ['\sID:\s*({login_id}[^\s]+?)\s+アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン', 'アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン\s*ID:\s*({login_id}[^\s]+?)\s+オブジェクト:'] |
| edit_regex_field | time |  | ['({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(AM|PM))', '({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),', '({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)'] |
| edit_regex_field | user |  | ['\sID:\s*({login_id}[^\s]+?)\s+アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン', 'アカウント名:\s*({user}(SYSTEM|LOCAL SERVICE|ANONYMOUS LOGON)|([\w\.\-\!\#\^\~]{1,40}\$?))\s*アカウント\s+ドメイン:\s*({domain}((NT AUTHORITY)|[^\s]+?))\s+ログオン\s*ID:\s*({login_id}[^\s]+?)\s+オブジェクト:'] |