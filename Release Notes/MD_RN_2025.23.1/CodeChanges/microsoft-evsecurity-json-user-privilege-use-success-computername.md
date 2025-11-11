# Code Changes for microsoft-evsecurity-json-user-privilege-use-success-computername (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'privileges', 'result', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)', 'SubjectDomainName\\?\"+:\\?\"+(|-|NT Service|NT AUTHORITY|({domain}({src_domain}[^\\]+)))\\?\"'] |
| edit_regex_field | src_domain |  | ['SubjectDomainName\\?\"+:\\?\"+(|-|NT Service|NT AUTHORITY|({domain}({src_domain}[^\\]+)))\\?\"'] |
| edit_regex_field | src_user |  | ['SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| added_regex_field | user |  | ['SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?"'] |
| removed_attribute | DupFields |  | N/A |