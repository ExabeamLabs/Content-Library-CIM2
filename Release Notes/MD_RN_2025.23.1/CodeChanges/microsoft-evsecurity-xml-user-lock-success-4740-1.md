# Code Changes for microsoft-evsecurity-xml-user-lock-success-4740-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | account |  | ['Account That Was Locked Out:\s*([\\t]*)Security ID:\s*([\\t]*)({user_sid}[^:]+?)\s*([\\t]*)Account Name:\s*([\\t]*)({account}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Additional'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?:\\+)?({domain}[^<=\s]+)(<|\s)'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<', 'Subject:[^=]+?Account Name:\s*([\\t]*)({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*([\\t]*)Account Domain:\s*(?=\w|([\\t]*)|NA)({src_domain}[^:]+?)\s*([\\t]*)Logon ID:\s*({login_id}[^:]+?)\s*Account That Was'] |
| edit_regex_field | src_host |  | ['Caller Computer Name:\s*([\\t]*)(?:\\+)?({src_host}[^<=\s]+)(<|\s)'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}[^<]+)<', 'Subject:[^=]+?Account Name:\s*([\\t]*)({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*([\\t]*)Account Domain:\s*(?=\w|([\\t]*)|NA)({src_domain}[^:]+?)\s*([\\t]*)Logon ID:\s*({login_id}[^:]+?)\s*Account That Was'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)<', 'Subject:[^=]+?Account Name:\s*([\\t]*)({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*([\\t]*)Account Domain:\s*(?=\w|([\\t]*)|NA)({src_domain}[^:]+?)\s*([\\t]*)Logon ID:\s*({login_id}[^:]+?)\s*Account That Was'] |