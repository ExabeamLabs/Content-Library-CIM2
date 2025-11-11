# Code Changes for microsoft-evsecurity-xml-user-privilege-assign-success-4672 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'privileges', 'result', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | src_user |  | ['<Data Name(\\\/)?=(\'|")SubjectUserName(\'|")>(NETWORK SERVICE|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| added_regex_field | user |  | ['<Data Name(\\\/)?=(\'|")SubjectUserName(\'|")>(NETWORK SERVICE|(\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |