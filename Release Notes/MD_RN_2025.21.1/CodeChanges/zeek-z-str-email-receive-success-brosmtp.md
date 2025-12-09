# Code Changes for zeek-z-str-email-receive-success-brosmtp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'email_address', 'email_domain', 'email_recipients', 'email_subject', 'orig_user', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['({alert_type}({alert_name}bro_smtp))'] |
| edit_regex_field | user |  | ['(?:[^\t]+\t){12}.*?<({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | alert_type |  | ['({alert_type}({alert_name}bro_smtp))'] |
| added_regex_field | orig_user |  | ['(?:[^\t]+\t){12}.*?<({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |