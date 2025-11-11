# Code Changes for microsoft-evsecurity-json-user-privilege-use-success-4674 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'category', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_id', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'severity', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName"*:"*({src_domain}({domain}[^"]+))'] |
| edit_regex_field | user |  | ['"SubjectUserName"*:"*(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName"*:"*({src_domain}({domain}[^"]+))'] |
| added_regex_field | src_user |  | ['"SubjectUserName"*:"*(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |