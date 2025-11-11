# Code Changes for microsoft-exchange-cef-email-send-originating (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'host', 'orig_user', 'result', 'time', 'user'] |
| edit_regex_field | email_address |  | ['\scs6=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+=', '\ssuser=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+\w+='] |
| edit_regex_field | email_domain |  | ['\scs6=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+=', '\ssuser=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+\w+='] |
| edit_regex_field | orig_user |  | ['\scs6=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| added_regex_field | user |  | ['\scs6=(({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+='] |
| removed_attribute | DupFields |  | N/A |