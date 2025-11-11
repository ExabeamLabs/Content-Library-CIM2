# Code Changes for microsoft-evsecurity-kv-group-member-add-success-wls (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_host', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'src_domain', 'src_user', 'time', 'user', 'user_dn', 'user_ou', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName="+({src_domain}({domain}[^"]+))"'] |
| edit_regex_field | event_code |  | ['EventID="+({group_type}({event_code}[^"]+))"'] |
| edit_regex_field | host |  | ['Computer="+({dest_host}({host}[^"]+))"'] |
| edit_regex_field | user |  | ['SubjectUserName="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_host |  | ['Computer="+({dest_host}({host}[^"]+))"'] |
| added_regex_field | group_type |  | ['EventID="+({group_type}({event_code}[^"]+))"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName="+({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['SubjectUserName="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |