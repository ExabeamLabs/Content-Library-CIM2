# Code Changes for microsoft-evtaskscheduler-xml-scheduled-task-create-fail-104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_severity', 'channel', 'domain', 'event_code', 'event_name', 'host', 'process_id', 'result', 'run_level', 'src_domain', 'src_host', 'src_ip', 'src_user', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<SubjectDomainName>(NT AUTHORITY|({src_domain}({domain}[^<]+)))'] |
| edit_regex_field | host |  | ['<Computer>({src_host}({host}[\w\-.]+))', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| edit_regex_field | src_host |  | ['<Computer>(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-\.]+))', '<Computer>({src_host}({host}[\w\-.]+))', '<\d+>\w+ \d+ \d\d:\d\d:\d\d ({src_host}({host}[\w_\-\.]+))'] |
| edit_regex_field | user |  | ['<SubjectUserName>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| added_regex_field | src_domain |  | ['<SubjectDomainName>(NT AUTHORITY|({src_domain}({domain}[^<]+)))'] |
| added_regex_field | src_user |  | ['<SubjectUserName>(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))'] |
| removed_attribute | DupFields |  | N/A |