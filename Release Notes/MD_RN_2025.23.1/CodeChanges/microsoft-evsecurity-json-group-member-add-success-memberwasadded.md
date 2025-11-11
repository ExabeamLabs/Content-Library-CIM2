# Code Changes for microsoft-evsecurity-json-group-member-add-success-memberwasadded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'account_id', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'result', 'src_domain', 'src_user', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | domain |  | ['"Account":"(({domain}[^\\\s"]+)\\+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| edit_regex_field | host |  | ['"hostname":"({dest_host}({host}[\w\-.]+))"'] |
| edit_regex_field | user |  | ['"Account":"(({domain}[^\\\s"]+)\\+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_host |  | ['"hostname":"({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['"Account":"(({domain}[^\\\s"]+)\\+)?({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', '"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |