# Code Changes for microsoft-evsecurity-kv-share-access-success-5140-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'd_name', 'd_parent', 'dest_host', 'domain', 'event_code', 'file_type', 'host', 'login_id', 'result', 'share_name', 'share_path', 'src_domain', 'src_ip', 'src_port', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| edit_regex_field | host |  | ['({dest_host}({host}[^\s]+?))\s+(Detailed File Share|File Share)'] |
| edit_regex_field | user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[^\s]+?))\s+(Detailed File Share|File Share)'] |
| added_regex_field | src_domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| added_regex_field | src_user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| removed_attribute | DupFields |  | N/A |