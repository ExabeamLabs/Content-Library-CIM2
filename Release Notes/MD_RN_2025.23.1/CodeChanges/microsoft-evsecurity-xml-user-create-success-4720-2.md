# Code Changes for microsoft-evsecurity-xml-user-create-success-4720-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_id', 'account_name', 'dest_domain', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | account_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>({dest_domain}({account_domain}[^<]+))<'] |
| edit_regex_field | account_name |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({account_name}[^<]+))<'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| added_regex_field | dest_domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>({dest_domain}({account_domain}[^<]+))<'] |
| added_regex_field | dest_user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({dest_user}({account_name}[^<]+))<'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))<'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |