# Code Changes for microsoft-evsecurity-kv-user-delete-fail-wls (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'login_id', 'src_domain', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | dest_user |  | ['TargetUserName="+({account_name}({dest_user}[^\"]+))"'] |
| edit_regex_field | domain |  | ['SubjectDomainName="+({src_domain}({domain}[^\"]+))"'] |
| edit_regex_field | user |  | ['SubjectUserName="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | account_name |  | ['TargetUserName="+({account_name}({dest_user}[^\"]+))"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName="+({src_domain}({domain}[^\"]+))"'] |
| added_regex_field | src_user |  | ['SubjectUserName="+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |