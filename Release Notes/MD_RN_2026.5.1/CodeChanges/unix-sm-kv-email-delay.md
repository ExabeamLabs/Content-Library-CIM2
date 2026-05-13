# Code Changes for unix-sm-kv-email-delay (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_email_address |  | ['to=(\w+,|)<?(({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\;,\|\>]+))?'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|Message|({host}[\w.\-]+)))\s+', '\w+ \d{2} \d{2}:\d{2}:\d{2} (Message forwarded from )?(::ffff:)?({host}[\w.\-]+):? \S+ ({alert_id}\S+?):', '\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?(Message|({host}[\w\-.]+))\s'] |
| edit_regex_field | host_ip |  | ['\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|Message|({host}[\w.\-]+)))\s+'] |