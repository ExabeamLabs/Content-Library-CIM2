# Code Changes for cyberark-pam-mix-user-switch-success-retrievepassword (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'action', 'dest_host', 'dest_user', 'domain', 'email_address', 'email_domain', 'event_code', 'gateway_station', 'host', 'result_reason', 'safe_value', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_user |  | ['\sFile=(({domain}[^\\]+)\\)?[^\-]+\-({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=', '\sFile=[^=]+\-({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | domain |  | ['\sFile=(({domain}[^\\]+)\\)?[^\-]+\-({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=', 'usrName=(({domain}[^\\=]+)(\\)+)?(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| edit_regex_field | host |  | ['(\d\d:\d\d:\d\d|\d\d\d\d-\d\d-\d\d\w\d\d:\d\d:\d\d\w) ({dest_host}({host}[\w\-.]+)) (LEEF|CEF)', '({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d))\s*({dest_host}({host}[\w\-.]+))\s*LEEF'] |
| edit_regex_field | time |  | ['({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d))\s*({dest_host}({host}[\w\-.]+))\s*LEEF', '({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)'] |
| added_regex_field | account |  | ['\sFile=(({domain}[^\\]+)\\)?[^\-]+\-({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+=', '\sFile=[^=]+\-({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+='] |
| added_regex_field | dest_host |  | ['(\d\d:\d\d:\d\d|\d\d\d\d-\d\d-\d\d\w\d\d:\d\d:\d\d\w) ({dest_host}({host}[\w\-.]+)) (LEEF|CEF)', '({time}(\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ|\w+\s+\d\d\s+\d\d:\d\d:\d\d))\s*({dest_host}({host}[\w\-.]+))\s*LEEF'] |
| removed_attribute | DupFields |  | N/A |