# Code Changes for microsoft-evsecurity-json-scheduled-task-create-success-4698 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_domain', 'account_name', 'additional_info', 'arg', 'dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_domain', 'src_user', 'task_name', 'thread_id', 'time', 'triggers', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^\"]+))"'] |
| edit_regex_field | host |  | ['"Computer(Name)?":"({dest_host}({host}[\w\-.]+))', '"Hostname":"({dest_host}({host}[\w.-]+?))"'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | dest_host |  | ['"Computer(Name)?":"({dest_host}({host}[\w\-.]+))', '"Hostname":"({dest_host}({host}[\w.-]+?))"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^\"]+))"'] |
| added_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |