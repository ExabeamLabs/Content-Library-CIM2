# Code Changes for microsoft-exchange-cef-email-receive-incoming (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'host', 'orig_user', 'result', 'return_path', 'src_ip', 'time', 'user'] |
| edit_regex_field | email_address |  | ['\sduser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '\ssuser=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+\w+='] |
| edit_regex_field | email_domain |  | ['\sduser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| edit_regex_field | orig_user |  | ['\sduser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | user |  | ['\sduser=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |