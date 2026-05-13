# Code Changes for microsoft-evsecurity-json-user-privilege-assign-success-4673-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'event_id', 'event_name', 'host', 'login_id', 'privileges', 'process_dir', 'process_id', 'process_name', 'process_path', 'provider_name', 'result', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid', 'user_upn'] |
| edit_regex_field | dest_host |  | ['"Computer":\s*"({dest_host}({host}[\w\-.]+))"', 'exa_json_path=$.Computer,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| edit_regex_field | event_name |  | ['({event_name}A privileged service was called)', 'exa_json_path=$.Message,exa_regex=({event_name}A privileged service was called)'] |
| edit_regex_field | host |  | ['"Computer":\s*"({dest_host}({host}[\w\-.]+))"', 'exa_json_path=$.Computer,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| edit_regex_field | process_dir |  | ['"process.process_name":\s*"({process_path}({process_dir}[^"]*)\\+({process_name}[^"\\\/]+))', 'exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}(?:[^";]+)?[\\\/]+)?({process_name}[^\\\/";]+?))$'] |
| edit_regex_field | process_name |  | ['"process.process_name":\s*"({process_path}({process_dir}[^"]*)\\+({process_name}[^"\\\/]+))', 'exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}(?:[^";]+)?[\\\/]+)?({process_name}[^\\\/";]+?))$'] |
| edit_regex_field | process_path |  | ['"process.process_name":\s*"({process_path}({process_dir}[^"]*)\\+({process_name}[^"\\\/]+))', 'exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}(?:[^";]+)?[\\\/]+)?({process_name}[^\\\/";]+?))$'] |
| edit_regex_field | time |  | ['"TimeCreated":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_json_path=$.TimeCreated,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |
| edit_regex_field | user |  | ['"subject.account_name":"(-|({user_upn}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))', 'exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| added_regex_field | channel |  | ['"Channel":\s*"({channel}[^"]+)'] |
| added_regex_field | domain |  | ['"subject.account_domain":\s*"({domain}[^"]+)', '"subject.account_name":"(-|({user_upn}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))'] |
| added_regex_field | event_code |  | ['"EventID":\s*"({event_code}[^"]+)'] |
| added_regex_field | event_id |  | ['"EventRecordID":\s*"({event_id}[^"]+)'] |
| added_regex_field | login_id |  | ['"subject.logon_id":"({login_id}[^"]+)'] |
| added_regex_field | privileges |  | ['privileges":\s*"({privileges}[^"]+)'] |
| added_regex_field | process_id |  | ['"ProcessID":\s*"({process_id}[^"]+)', '"process.process_id":\s*"({process_id}[^"]+)'] |
| added_regex_field | provider_name |  | ['"ProviderName":\s*"({provider_name}[^"]+)'] |
| added_regex_field | result |  | ['"Keywords":\s*"({result}[^"]+)'] |
| added_regex_field | task_name |  | ['"Task":\s*"({task_name}[^"]+)'] |
| added_regex_field | thread_id |  | ['"ThreadID":\s*"({thread_id}[^"]+)'] |
| added_regex_field | user_sid |  | ['"subject.security_id":\s*"({user_sid}[^"]+)'] |
| added_regex_field | user_upn |  | ['"subject.account_name":"(-|({user_upn}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({=user}[^"]+))'] |