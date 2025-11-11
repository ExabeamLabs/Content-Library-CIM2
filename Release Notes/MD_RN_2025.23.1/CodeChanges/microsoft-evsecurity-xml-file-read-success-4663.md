# Code Changes for microsoft-evsecurity-xml-file-read-success-4663 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'registry_key', 'registry_path', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\\)?"+SubjectDomainName(\\)?"+>(NT AUTHORITY|({src_domain}({domain}[^<]+)))<\/Data>'] |
| edit_regex_field | host |  | ['"Computer"+:"+({src_host}({host}[\w\-.]+))'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\\)?"+SubjectUserName(\\)?"+>(LOCAL SERVICE|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\\)?"+SubjectDomainName(\\)?"+>(NT AUTHORITY|({src_domain}({domain}[^<]+)))<\/Data>'] |
| added_regex_field | src_host |  | ['"Computer"+:"+({src_host}({host}[\w\-.]+))'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\\)?"+SubjectUserName(\\)?"+>(LOCAL SERVICE|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<\/Data>'] |
| removed_attribute | DupFields |  | N/A |