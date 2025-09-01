# Code Changes for microsoft-evsecurity-json-share-access-success-5140-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | d_name |  | ['<Data Name\\*=(\'|")ShareLocalPath(\'|")>(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+)\\)?({d_name}\s*\S[^\\<]+?))\\?)</Data>'] |
| edit_regex_field | d_parent |  | ['<Data Name\\*=(\'|")ShareLocalPath(\'|")>(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+)\\)?({d_name}\s*\S[^\\<]+?))\\?)</Data>'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}.+?)</Data>'] |
| edit_regex_field | file_type |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({file_type}.+?)</Data>'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}.+?)</Data>'] |
| edit_regex_field | share_name |  | ['<Data Name\\*=(\'|")ShareName(\'|")>(?:[\\\*]+)?({share_name}.+?)</Data>'] |
| edit_regex_field | share_path |  | ['<Data Name\\*=(\'|")ShareLocalPath(\'|")>(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}.+)\\)?({d_name}\s*\S[^\\<]+?))\\?)</Data>'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")IpAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>'] |
| edit_regex_field | src_port |  | ['(\'|")IpPort(\'|")>({src_port}\d+)', '<Data Name\\*=(\'|")IpAddress(\'|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</Data>', 'Source Port(=|:)\s*(\\t)*({src_port}\d+)'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |