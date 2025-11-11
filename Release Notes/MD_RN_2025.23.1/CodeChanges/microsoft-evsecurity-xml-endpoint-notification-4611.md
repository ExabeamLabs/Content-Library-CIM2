# Code Changes for microsoft-evsecurity-xml-endpoint-notification-4611 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^"\s<]+))<'] |
| edit_regex_field | user |  | ['(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| added_regex_field | src_domain |  | ['(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^"\s<]+))<'] |
| added_regex_field | src_user |  | ['(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| removed_attribute | DupFields |  | N/A |