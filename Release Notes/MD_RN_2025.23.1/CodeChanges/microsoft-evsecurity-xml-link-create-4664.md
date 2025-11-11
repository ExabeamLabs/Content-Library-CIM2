# Code Changes for microsoft-evsecurity-xml-link-create-4664 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'login_id', 'result', 'run_level', 'src_domain', 'src_user', 'time', 'transaction_id', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^\'<\s"]+))<'] |
| edit_regex_field | user |  | ['(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| added_regex_field | src_domain |  | ['(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^\'<\s"]+))<'] |
| added_regex_field | src_user |  | ['(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| removed_attribute | DupFields |  | N/A |