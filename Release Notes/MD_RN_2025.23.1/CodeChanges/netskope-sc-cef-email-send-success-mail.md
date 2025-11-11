# Code Changes for netskope-sc-cef-email-send-success-mail (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'app', 'auth_method', 'browser', 'bytes', 'dest_email_address', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'email_recipients', 'file_type', 'from_user_at', 'full_name', 'location', 'object', 'operation', 'os', 'referrer', 'site_at', 'src_host', 'src_ip', 'src_port', 'time', 'url', 'user', 'web_domain'] |
| edit_regex_field | email_address |  | ['"from_user":"({from_user_at}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"', '"user":\s*"(({from_user_at}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | email_domain |  | ['"user":\s*"(({from_user_at}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"user":\s*"(({from_user_at}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | from_user_at |  | ['"from_user":"({from_user_at}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"', '"user":\s*"(({from_user_at}({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |