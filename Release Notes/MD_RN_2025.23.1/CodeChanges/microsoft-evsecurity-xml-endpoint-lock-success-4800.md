# Code Changes for microsoft-evsecurity-xml-endpoint-lock-success-4800 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'category', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'process_id', 'run_level', 'time', 'user', 'user_sid'] |
| edit_regex_field | dest_domain |  | ['<Hostname>({dest_host}({host}[^\.\<]+))\.({dest_domain}({domain}[^\s\<]+))<', '<TargetDomainName>({dest_domain}[^\<]+)<', 'Data Name(\\)?=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))'] |
| edit_regex_field | dest_host |  | ['<Computer>({dest_host}({host}[\w\-.]+))', '<Hostname>({dest_host}({host}[^\.\<]+))\.({dest_domain}({domain}[^\s\<]+))<'] |
| edit_regex_field | domain |  | ['<Hostname>({dest_host}({host}[^\.\<]+))\.({dest_domain}({domain}[^\s\<]+))<', 'Data Name(\\)?=(\'|")TargetDomainName(\'|")>({dest_domain}({domain}[^<]+))'] |
| edit_regex_field | host |  | ['<Computer>({dest_host}({host}[\w\-.]+))', '<Hostname>({dest_host}({host}[^\.\<]+))\.({dest_domain}({domain}[^\s\<]+))<', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)'] |
| edit_regex_field | login_id |  | ['<TargetLogonId>({dest_login_id}({login_id}[^\<]+))<', 'Data Name(\\)?=(\'|")TargetLogonId(\'|")>({dest_login_id}({login_id}[^<]+))'] |
| edit_regex_field | user |  | ['<TargetUserName>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', 'Data Name(\\)?=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user_sid |  | ['<TargetUserSid>({dest_user_sid}({user_sid}[^\<]+))<', 'Data Name(\\)?=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))'] |
| added_regex_field | dest_login_id |  | ['<TargetLogonId>({dest_login_id}({login_id}[^\<]+))<', 'Data Name(\\)?=(\'|")TargetLogonId(\'|")>({dest_login_id}({login_id}[^<]+))'] |
| added_regex_field | dest_user |  | ['<TargetUserName>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', 'Data Name(\\)?=(\'|")TargetUserName(\'|")>({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_user_sid |  | ['<TargetUserSid>({dest_user_sid}({user_sid}[^\<]+))<', 'Data Name(\\)?=(\'|")TargetUserSid(\'|")>({dest_user_sid}({user_sid}[^<]+))'] |
| removed_attribute | DupFields |  | N/A |