# Code Changes for microsoft-evsecurity-xml-user-lock-success-4740-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'run_level', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<', 'Subject:[^=]+?Account Name:\s*([\\t]*)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*([\\t]*)Account Domain:\s*(?=\w|([\\t]*)|NA)({domain}[^:]+?)\s*([\\t]*)Logon ID:\s*({login_id}[^:]+?)\s*Account That Was'] |
| removed_regex_field | src_domain |  | [] |
| edit_regex_field | src_host |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?:\\+)?({src_host}[^<=\s]+)(<|\s)', 'Caller Computer Name:\s*([\\t]*)(?:\\+)?({src_host}[^<=\s]+)(<|\s)'] |
| removed_regex_field | src_user |  | [] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<', 'Subject:[^=]+?Account Name:\s*([\\t]*)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*([\\t]*)Account Domain:\s*(?=\w|([\\t]*)|NA)({domain}[^:]+?)\s*([\\t]*)Logon ID:\s*({login_id}[^:]+?)\s*Account That Was'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")TargetSid(\'|")>({user_sid}[^<]+)<', 'Account That Was Locked Out:\s*([\\t]*)Security ID:\s*([\\t]*)({user_sid}[^:]+?)\s*([\\t]*)Account Name:\s*([\\t]*)({account}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Additional'] |
| added_regex_field | account |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>({account}[\w\.\-\!\#\^\~]{1,40}\$?)<', 'Account That Was Locked Out:\s*([\\t]*)Security ID:\s*([\\t]*)({user_sid}[^:]+?)\s*([\\t]*)Account Name:\s*([\\t]*)({account}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Additional'] |
| added_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<', 'Subject:[^=]+?Account Name:\s*([\\t]*)({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*([\\t]*)Account Domain:\s*(?=\w|([\\t]*)|NA)({domain}[^:]+?)\s*([\\t]*)Logon ID:\s*({login_id}[^:]+?)\s*Account That Was'] |
| removed_attribute | DupFields |  | N/A |