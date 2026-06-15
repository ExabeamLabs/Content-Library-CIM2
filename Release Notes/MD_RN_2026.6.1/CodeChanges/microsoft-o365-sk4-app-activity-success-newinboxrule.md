# Code Changes for microsoft-o365-sk4-app-activity-success-newinboxrule (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'correlation_id', 'dest_domain', 'domain', 'email_address', 'filter_key_words', 'host', 'mailbox_name', 'object', 'operation', 'result', 'src_ip', 'src_port', 'target', 'target_domain', 'time', 'user'] |
| edit_regex_field | domain |  | ['"UserId":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?(@({domain}[^"]+))?))\s*"'] |
| edit_regex_field | email_address |  | ['"UserId":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?(@({domain}[^"]+))?))\s*"', 'suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'user_email="({email_address}[^@"]+@[^\."]+\.[^"]+)"'] |
| edit_regex_field | object |  | ['"ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))', 'ObjectId":"(Unknown|Not Available|({object}[^"]+))'] |
| edit_regex_field | target |  | ['"Name":"ForwardTo".+?"Value":"(?:smtp:)?({target}[^"]+)"', '"TargetUserOrGroupName":"({target}[^"]+)"'] |
| edit_regex_field | user |  | ['"UserId":"(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?(@({domain}[^"]+))?))\s*"', 'suser=(({email_address}[A-Za-z0-9!#$%&\'+\/=?^_`~.-]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'user="({user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | mailbox_name |  | ['"ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))'] |
| added_regex_field | target_domain |  | ['"TargetUserOrGroupName":"([^@]+)@({target_domain}[^"]*?)"'] |