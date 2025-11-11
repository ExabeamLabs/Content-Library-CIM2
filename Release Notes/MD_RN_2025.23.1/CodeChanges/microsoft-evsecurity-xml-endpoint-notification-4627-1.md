# Code Changes for microsoft-evsecurity-xml-endpoint-notification-4627-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_email_address', 'dest_user', 'dest_user_sid', 'domain', 'email_address', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'login_type', 'process_id', 'result', 'run_level', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))<'] |
| edit_regex_field | email_address |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name(\\)?=(\'|")SubjectUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<', '<Data Name(\\)?=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<'] |
| added_regex_field | dest_domain |  | ['<Data Name(\\)?=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))<'] |
| added_regex_field | dest_email_address |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| added_regex_field | dest_user |  | ['<Data Name(\\)?=(\'|")TargetUserName(\'|")>(({dest_email_address}({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| added_regex_field | dest_user_sid |  | ['<Data Name(\\)?=(\'|")SubjectUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<', '<Data Name(\\)?=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))<'] |
| removed_attribute | DupFields |  | N/A |