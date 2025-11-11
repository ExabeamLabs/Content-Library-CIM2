# Code Changes for microsoft-evsecurity-sk4-user-password-reset-success-4724 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectAccount":"(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"SubjectDomainName":"({domain}({src_domain}[^"]+))"'] |
| edit_regex_field | host |  | ['"Computer":"({dest_host}({host}[^"]+))"'] |
| edit_regex_field | src_domain |  | ['"SubjectDomainName":"({domain}({src_domain}[^"]+))"'] |
| edit_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| edit_regex_field | user |  | ['"SubjectAccount":"(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"', '"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | dest_host |  | ['"Computer":"({dest_host}({host}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |