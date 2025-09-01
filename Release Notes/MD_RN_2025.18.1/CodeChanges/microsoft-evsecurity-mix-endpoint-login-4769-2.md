# Code Changes for microsoft-evsecurity-mix-endpoint-login-4769-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['<Data Name\\*=(\'|")ServiceName(\'|")>({dest_host}[\w\-.]+\$)</Data>'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")TargetDomainName(\'|")>(?=\w)({domain}[^<]+)</Data>', '<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^<]+))?</Data>'] |
| edit_regex_field | result_code |  | ['<Data Name\\*=(\'|")Status(\'|")>({result_code}[^<]+)</Data>'] |
| edit_regex_field | service_name |  | ['<Data Name\\*=(\'|")ServiceName(\'|")>({service_name}[^<]+)</Data>'] |
| edit_regex_field | src_ip |  | ['<Data Name\\*=(\'|")IpAddress(\'|")>(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | src_port |  | ['<Data Name\\*=(\'|")IpAddress(\'|")>(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'] |
| edit_regex_field | ticket_encryption_type |  | ['<Data Name\\*=(\'|")TicketEncryptionType(\'|")>({ticket_encryption_type}[^<]+)</Data>'] |
| edit_regex_field | ticket_options |  | ['<Data Name\\*=(\'|")TicketOptions(\'|")>({ticket_options}[^<]+)</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")TargetUserName(\'|")>(?=\w)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^<]+))?</Data>'] |