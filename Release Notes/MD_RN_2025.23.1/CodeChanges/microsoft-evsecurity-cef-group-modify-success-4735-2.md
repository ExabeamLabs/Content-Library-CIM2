# Code Changes for microsoft-evsecurity-cef-group-modify-success-4735-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'domain', 'event_code', 'event_id', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| edit_regex_field | user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| added_regex_field | src_domain |  | ['"subjectDomainName":"({src_domain}({domain}[^"\s]+?))\s*"'] |
| added_regex_field | src_user |  | ['"subjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*"'] |
| removed_attribute | DupFields |  | N/A |