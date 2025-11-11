# Code Changes for microsoft-evsecurity-mix-user-lock-success-4740 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'src_domain', 'src_host', 'src_ip', 'src_user', 'time', 'user', 'user_sid'] |
| removed_regex_field | dest_user |  | [] |
| edit_regex_field | src_user |  | ['Account Name:(\\t|\\r|\\n|\s)*({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'Subject(:|=).+?Account Name(:|=)(\\[rnt]|\s)*({src_user}[^\s]*?)(\\[rnt]|\s)*[\s;]*Account Domain(:|=)', 'Subject:.+?Account Name:(\\t|\\r|\\n|\s)*({src_user}[^:]+?)(\\t|\\r|\\n|\s)*Account Domain:(\\t|\\r|\\n|\s)*(?=\w)({src_domain}[^:]+?)(\\t|\\r|\\n|\s)*Logon ID:(\\t|\\r|\\n|\s)*({login_id}[^\s\\]+)(\\t|\\r|\\n|\s)*'] |
| edit_regex_field | user |  | ['"targetUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', 'Locked Out:(\\[rnt]|\s)*Security ID:(\\[rnt]|\s)*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+?))\}?(\\[rnt]|\s)*Account Name:(\\[rnt]|\s)*(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\[rnt]|\s)*Additional'] |
| edit_regex_field | user_sid |  | ['Locked Out:(\\[rnt]|\s)*Security ID:(\\[rnt]|\s)*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+?))\}?(\\[rnt]|\s)*Account Name:(\\[rnt]|\s)*(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\[rnt]|\s)*Additional', 'Locked Out:(\\n)*\s+Security ID:\s*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+))\}?(\\n)*\s+Account Name:\s*(?=\w)({account}[\w\.\-\!\#\^\~]{1,40}\$?)(\\n)*\s*Additional'] |
| added_regex_field | account |  | ['Locked Out:(\\n)*\s+Security ID:\s*(%\{)?({user_sid}([\w\d\-]+?)|([^\s]+))\}?(\\n)*\s+Account Name:\s*(?=\w)({account}[\w\.\-\!\#\^\~]{1,40}\$?)(\\n)*\s*Additional'] |