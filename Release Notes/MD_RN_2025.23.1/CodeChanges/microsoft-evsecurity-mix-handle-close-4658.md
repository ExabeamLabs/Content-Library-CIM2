# Code Changes for microsoft-evsecurity-mix-handle-close-4658 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'object_id', 'object_server', 'operation_type', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_domain', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(NT AUTHORITY|({src_domain}({domain}[^<>]+)))</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(NT AUTHORITY|({src_domain}({domain}[^<>]+)))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))</Data>'] |
| removed_attribute | DupFields |  | N/A |