# Code Changes for microsoft-evsecurity-xml-endpoint-activity-4660 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'host', 'login_id', 'object', 'object_class', 'object_id', 'object_server', 'process_dir', 'process_name', 'process_path', 'run_level', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}.+?))</Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}.+?))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |