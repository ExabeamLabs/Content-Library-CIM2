# Code Changes for microsoft-evapp-xml-app-activity-frontendhttpproxy (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'run_level', 'src_ip', 'src_port', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain | ['Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:'] | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({domain}[^<]+?))<', 'Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:'] |
| edit_regex_field | login_id | ['Logon ID:\s*({login_id}\S+)\s+'] | ['<Data Name(\\)?=(\'|")SubjectLogonId(\'|")>(-|({login_id}[^<]+?))<', 'Logon ID:\s*({login_id}\S+)\s+'] |
| edit_regex_field | result | ['<Keyword>({result}[^<]+)<'] | ['<Keyword>({result}[^<]+)<', '<Keywords>({result}[^<]+)<'] |
| edit_regex_field | user | ['Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:'] | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', 'Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:'] |
| added_regex_field | event_id | [] | ['<EventRecordID>({event_id}[^<]+)<\/EventRecordID>'] |