# Code Changes for microsoft-evsecurity-cef-group-member-remove-success-4733-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'group_type', 'host', 'login_id', 'result', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| edit_regex_field | user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | src_domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| added_regex_field | src_user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| removed_attribute | DupFields |  | N/A |