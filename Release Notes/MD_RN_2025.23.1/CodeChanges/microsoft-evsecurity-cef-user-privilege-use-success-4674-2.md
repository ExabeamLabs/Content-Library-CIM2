# Code Changes for microsoft-evsecurity-cef-user-privilege-use-success-4674-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\\)?"+SubjectDomainName(\\)?"+>(NT AUTHORITY|({src_domain}({domain}[^<]+)))<\/Data>'] |
| edit_regex_field | host |  | ['Computer"+:"+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\\)?"+SubjectUserName(\\)?"+>(LOCAL SERVICE|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| added_regex_field | dest_host |  | ['Computer"+:"+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\\)?"+SubjectDomainName(\\)?"+>(NT AUTHORITY|({src_domain}({domain}[^<]+)))<\/Data>'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\\)?"+SubjectUserName(\\)?"+>(LOCAL SERVICE|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |