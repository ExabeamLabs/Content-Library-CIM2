# Code Changes for microsoft-evsecurity-json-share-access-success-5140-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'accesses_code', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'file_type', 'host', 'login_id', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| edit_regex_field | accesses_code |  | ['({accesses_code}({access}4416))'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}.+?))</Data>'] |
| edit_regex_field | host |  | ['"Computer":"({dest_host}({host}[^"]+))'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | access |  | ['({accesses_code}({access}4416))'] |
| added_regex_field | dest_host |  | ['"Computer":"({dest_host}({host}[^"]+))'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}.+?))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |