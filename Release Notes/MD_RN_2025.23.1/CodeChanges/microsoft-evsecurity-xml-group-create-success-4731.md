# Code Changes for microsoft-evsecurity-xml-group-create-success-4731 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\?=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<>]+)))<'] |
| edit_regex_field | user |  | ['<Data Name\\?=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| added_regex_field | src_domain |  | ['<Data Name\\?=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<>]+)))<'] |
| added_regex_field | src_user |  | ['<Data Name\\?=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |