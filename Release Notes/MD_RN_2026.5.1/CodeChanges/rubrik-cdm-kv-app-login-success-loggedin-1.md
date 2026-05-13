# Code Changes for rubrik-cdm-kv-app-login-success-loggedin-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | auth_method |  | ['\] (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) [^\)]+?\) ({event_name}logged in) with ({auth_method}[^"]+?) from ({src_host}[\w.-]+?)\s*("|$)'] |
| edit_regex_field | email_address |  | ['\] (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) [^\)]+?\) ({event_name}logged in) with ({auth_method}[^"]+?) from ({src_host}[\w.-]+?)\s*("|$)'] |
| edit_regex_field | event_name |  | ['\] (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) [^\)]+?\) ({event_name}logged in) with ({auth_method}[^"]+?) from ({src_host}[\w.-]+?)\s*("|$)'] |
| edit_regex_field | src_host |  | ['\] (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) [^\)]+?\) ({event_name}logged in) with ({auth_method}[^"]+?) from ({src_host}[\w.-]+?)\s*("|$)'] |
| edit_regex_field | user |  | ['\] (({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) [^\)]+?\) ({event_name}logged in) with ({auth_method}[^"]+?) from ({src_host}[\w.-]+?)\s*("|$)'] |