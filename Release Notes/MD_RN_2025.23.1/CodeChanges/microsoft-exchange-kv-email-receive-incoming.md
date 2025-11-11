# Code Changes for microsoft-exchange-kv-email-receive-incoming (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'alert_name', 'alert_type', 'bytes', 'dest_email_address', 'dest_email_domain', 'dest_host', 'dest_ip', 'dest_port', 'dest_user', 'dest_user_full_name', 'direction', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'num_recipients', 'orig_user', 'result', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dest_email_address |  | ['recipient-address=({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)))'] |
| edit_regex_field | dest_email_domain |  | ['recipient-address=({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)))'] |
| edit_regex_field | dest_user |  | ['recipient-address=({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)))'] |
| edit_regex_field | dest_user_full_name |  | ['recipient-address=({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)))'] |
| added_regex_field | alert_type |  | ['\tsource=(?:|({alert_type}.+?))\t[\w\-]+='] |
| added_regex_field | orig_user |  | ['recipient-address=({orig_user}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)))'] |
| removed_attribute | DupFields |  | N/A |