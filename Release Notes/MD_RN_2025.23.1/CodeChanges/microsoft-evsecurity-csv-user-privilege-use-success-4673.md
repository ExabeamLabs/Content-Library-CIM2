# Code Changes for microsoft-evsecurity-csv-user-privilege-use-success-4673 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'host', 'login_id', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_user', 'time', 'user'] |
| edit_regex_field | domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| edit_regex_field | user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| added_regex_field | src_domain |  | ['SubjectDomainName:({src_domain}({domain}[^,]+)),'] |
| added_regex_field | src_user |  | ['SubjectUserName:({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)),'] |
| removed_attribute | DupFields |  | N/A |