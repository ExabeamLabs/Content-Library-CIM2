# Code Changes for microsoft-evsecurity-xml-key-5061-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'activity_id', 'channel', 'dest_user_sid', 'domain', 'error_code', 'event_code', 'event_id', 'event_name', 'failure_reason', 'file_path', 'group_domain', 'group_id', 'group_name', 'host', 'key_name', 'key_type', 'login_id', 'operation', 'process_id', 'provider_name', 'result', 'return_code', 'rule', 'rule_id', 'run_level', 'src_domain', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>', 'Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>', 'Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>((?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |