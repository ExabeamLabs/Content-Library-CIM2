# Code Changes for microsoft-evsecurity-json-user-privilege-use-success-4674-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'access_mask', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'object', 'object_server', 'object_type', 'ownership_privilege', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_ip', 'src_port', 'src_user', 'task_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['\"(SubjectDomainName)\"\s*:\s*\"(-|({src_domain}({domain}.+?)))\s*\"', 'exa_json_path=$.event_data.SubjectDomainName,exa_regex=(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\"]+)))\\?$'] |
| edit_regex_field | host |  | ['\"hostname\":\"({dest_host}({host}[\w\-.]*))'] |
| edit_regex_field | user |  | ['\"(SubjectUserName)\"\s*:\s*\"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\"', 'exa_json_path=$.event_data.SubjectUserName,exa_regex=(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?$'] |
| added_regex_field | dest_host |  | ['\"hostname\":\"({dest_host}({host}[\w\-.]*))'] |
| added_regex_field | src_domain |  | ['\"(SubjectDomainName)\"\s*:\s*\"(-|({src_domain}({domain}.+?)))\s*\"', 'exa_json_path=$.event_data.SubjectDomainName,exa_regex=(|-|NT Service|NT AUTHORITY|({src_domain}({domain}[^\"]+)))\\?$'] |
| added_regex_field | src_user |  | ['\"(SubjectUserName)\"\s*:\s*\"(-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s*\"', 'exa_json_path=$.event_data.SubjectUserName,exa_regex=(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?$'] |
| removed_attribute | DupFields |  | N/A |