# Code Changes for microsoft-evsecurity-xml-user-name-modify-4781 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'new_user_name', 'old_user_name', 'privileges', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+)))<'] |
| edit_regex_field | new_user_name |  | ['<Data Name\\*=(\'|")NewTargetUserName(\'|")>(-|({dest_user}({new_user_name}[^<]+)))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")NewTargetUserName(\'|")>(-|({dest_user}({new_user_name}[^<]+)))<'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+)))<'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |