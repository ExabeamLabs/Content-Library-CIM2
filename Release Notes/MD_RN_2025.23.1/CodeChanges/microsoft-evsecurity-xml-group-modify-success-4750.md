# Code Changes for microsoft-evsecurity-xml-group-modify-success-4750 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'group_domain', 'group_id', 'group_name', 'host', 'login_id', 'privileges', 'process_id', 'result', 'run_level', 'src_domain', 'src_user', 'sub_category', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |