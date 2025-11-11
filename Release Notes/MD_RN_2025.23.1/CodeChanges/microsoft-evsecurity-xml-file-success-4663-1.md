# Code Changes for microsoft-evsecurity-xml-file-success-4663-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'registry_key', 'registry_path', 'run_level', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*="SubjectDomainName">(?=\w)({src_domain}({domain}[^<]+))<'] |
| edit_regex_field | user |  | ['<Data Name\\*="SubjectUserName">(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| added_regex_field | src_domain |  | ['<Data Name\\*="SubjectDomainName">(?=\w)({src_domain}({domain}[^<]+))<'] |
| added_regex_field | src_user |  | ['<Data Name\\*="SubjectUserName">(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| removed_attribute | DupFields |  | N/A |