# Code Changes for microsoft-evsecurity-cef-file-permission-modify-4670 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'new_attribute', 'object_id', 'object_name', 'object_type', 'old_attribute', 'process_dir', 'process_id', 'process_name', 'process_path', 'resource', 'run_level', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"'] |
| removed_attribute | DupFields |  | N/A |