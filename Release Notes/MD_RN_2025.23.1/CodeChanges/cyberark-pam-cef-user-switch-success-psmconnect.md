# Code Changes for cyberark-pam-cef-user-switch-success-psmconnect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_domain', 'dest_email_address', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'domain', 'event_code', 'host', 'safe_value', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | dest_domain |  | ['\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+=', '\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | dest_email_address |  | ['\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| edit_regex_field | dest_user |  | ['\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+=', '\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | account |  | ['\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+=', '\sduser=(({dest_domain}[^\\=]+)[\\\/]+)?({account}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |