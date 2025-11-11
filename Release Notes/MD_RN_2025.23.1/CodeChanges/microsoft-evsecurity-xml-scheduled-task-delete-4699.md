# Code Changes for microsoft-evsecurity-xml-scheduled-task-delete-4699 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_domain', 'src_host', 'src_ip', 'src_port', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({domain}[^<]+?))<', '<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))', 'Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', '<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:'] |
| added_regex_field | src_domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({src_domain}({domain}[^<]+))'] |
| added_regex_field | src_user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |