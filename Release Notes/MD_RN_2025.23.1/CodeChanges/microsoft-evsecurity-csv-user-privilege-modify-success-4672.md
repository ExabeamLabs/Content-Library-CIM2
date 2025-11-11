# Code Changes for microsoft-evsecurity-csv-user-privilege-modify-success-4672 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'host', 'login_id', 'privileges', 'result', 'src_domain', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| edit_regex_field | user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| added_regex_field | src_domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| added_regex_field | src_user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| removed_attribute | DupFields |  | N/A |