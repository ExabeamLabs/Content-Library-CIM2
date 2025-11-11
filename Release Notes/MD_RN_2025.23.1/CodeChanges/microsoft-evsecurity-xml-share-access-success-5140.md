# Code Changes for microsoft-evsecurity-xml-share-access-success-5140 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'event_name', 'file_type', 'host', 'login_id', 'run_level', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['<Data Name(\\\/)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\\/)?=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name(\\\/)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+?))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name(\\\/)?=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |