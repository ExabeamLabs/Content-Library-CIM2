# Code Changes for microsoft-evsecurity-csv-endpoint-notification-success-4611 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'dest_host', 'domain', 'event_code', 'event_id', 'login_id', 'src_domain', 'src_user', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['SubjectDomainName="+(?=\w)({src_domain}({domain}[^"]+))"'] |
| edit_regex_field | user |  | ['SubjectUserName="+(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| added_regex_field | src_domain |  | ['SubjectDomainName="+(?=\w)({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['SubjectUserName="+(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"'] |
| removed_attribute | DupFields |  | N/A |