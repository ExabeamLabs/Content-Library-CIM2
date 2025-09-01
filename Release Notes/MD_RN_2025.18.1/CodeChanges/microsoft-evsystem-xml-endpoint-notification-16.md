# Code Changes for microsoft-evsystem-xml-endpoint-notification-16 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | login_id |  | ['Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<\/Data>'] |
| edit_regex_field | process_id |  | ['ProcessID\\*=(\'|")({process_id}\d+)(\'|")'] |
| edit_regex_field | result_code |  | ['<Data Name\\*=(\'|")FailureReason(\'|")>({result_code}[^<]+)<\/Data>'] |
| edit_regex_field | src_ip |  | ['Data Name\\*=(\'|")Ipaddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/Data>'] |
| edit_regex_field | src_port |  | ['Data Name\\*=(\'|")Ipaddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/Data>'] |
| edit_regex_field | user |  | ['Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['Security UserID\\*=(\'|")({user_sid}[^\'"]+)(\'|")'] |