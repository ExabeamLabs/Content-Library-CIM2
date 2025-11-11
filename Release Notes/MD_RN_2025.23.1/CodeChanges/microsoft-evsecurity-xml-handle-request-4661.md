# Code Changes for microsoft-evsecurity-xml-handle-request-4661 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'dest_host', 'domain', 'event_code', 'handle_id', 'host', 'login_id', 'object', 'object_server', 'object_type', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'properties', 'run_level', 'src_domain', 'src_user', 'time', 'transaction_id', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(NT AUTHORITY|({src_domain}({domain}[^<>]+)))<'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>(NT AUTHORITY|({src_domain}({domain}[^<>]+)))<'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))<'] |
| removed_attribute | DupFields |  | N/A |