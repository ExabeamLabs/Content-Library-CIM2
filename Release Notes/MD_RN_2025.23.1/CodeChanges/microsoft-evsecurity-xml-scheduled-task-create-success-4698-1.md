# Code Changes for microsoft-evsecurity-xml-scheduled-task-create-success-4698-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'arg', 'author', 'description', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'login_type_text', 'process_dir', 'process_name', 'process_path', 'run_level', 'src_domain', 'src_user', 'task_name', 'time', 'triggers', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(?=\w)({src_domain}({domain}[^<]+))</Data>'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(?=\w)({src_domain}({domain}[^<]+))</Data>'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(?=\w)({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>'] |
| removed_attribute | DupFields |  | N/A |