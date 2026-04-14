# Code Changes for microsoft-evsecurity-sk4-endpoint-activity-success-microsoftwindowssecurityauditing (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'channel', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'process_dir', 'process_id', 'process_name', 'process_path', 'result', 'src_domain', 'src_user', 'time', 'transaction_id', 'user', 'user_sid'] |
| edit_regex_field | event_name |  | ['"message":"({event_name}[^:"]+)', 'exa_json_path=$..Message,exa_regex=({event_name}[^.]+)'] |
| edit_regex_field | host |  | ['"Hostname":"({host}[\w\-.]+)"', 'exa_json_path=$.Hostname,exa_regex=^({host}[\w\-.]+)$'] |
| edit_regex_field | process_dir |  | ['"ProcessName":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"', 'exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$', 'exa_json_path=$..param1,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$'] |
| edit_regex_field | process_name |  | ['"ProcessName":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"', 'exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$', 'exa_json_path=$..param1,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$'] |
| edit_regex_field | process_path |  | ['"ProcessName":"({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"', 'exa_json_path=$..ProcessName,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$', 'exa_json_path=$..param1,exa_regex=^({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))$'] |
| edit_regex_field | src_user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | time |  | ['"EventTime":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)', '"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)', 'exa_json_path=$.EventTime,exa_regex=({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)', 'exa_json_path=$.TimeCreated,exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |
| edit_regex_field | user |  | ['"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))', 'exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | category |  | ['"category":"({category}[^"]+)"'] |
| added_regex_field | channel |  | ['"Channel":"({channel}[^"]+)"'] |
| added_regex_field | domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| added_regex_field | event_code |  | ['"EventID":({event_code}\d+)'] |
| added_regex_field | login_id |  | ['"SubjectLogonId":"({login_id}[^"]+)'] |
| added_regex_field | process_id |  | ['"ProcessId":"({process_id}[^"]+)'] |
| added_regex_field | result |  | ['"EventType":"({result}[^"]+)"'] |
| added_regex_field | src_domain |  | ['"SubjectDomainName":"({src_domain}({domain}[^"]+))"'] |
| added_regex_field | transaction_id |  | ['"TransactionId":"({transaction_id}[^"]+)"'] |
| added_regex_field | user_sid |  | ['"SubjectUserSid":"({user_sid}[^"]+)"'] |