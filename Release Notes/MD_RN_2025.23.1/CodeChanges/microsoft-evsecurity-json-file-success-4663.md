# Code Changes for microsoft-evsecurity-json-file-success-4663 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'domain', 'event_code', 'event_name', 'file_dir', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'src_domain', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |