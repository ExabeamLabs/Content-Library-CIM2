# Code Changes for microsoft-evsecurity-json-share-access-success-5140-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'app', 'dest_domain', 'dest_host', 'dest_login_id', 'dest_user', 'dest_user_sid', 'domain', 'event_code', 'event_id', 'event_name', 'file_type', 'host', 'login_id', 'login_type', 'operation_id', 'os', 'privileges', 'process_id', 'provider_name', 'result', 'share_name', 'sid_history', 'src_domain', 'src_host', 'src_port', 'src_user', 'task_name', 'thread_id', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['"+SubjectDomainName\"+:\"+({src_domain}({domain}[^\"]+))'] |
| edit_regex_field | host |  | ['"hostname\"+:\"+({dest_host}({host}[\w\-.]+))', 'exa_json_path=$..hostname,exa_regex=^({dest_host}({host}[\w\-.]+))$', 'exa_json_path=$.host.hostname,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| edit_regex_field | user |  | ['"+SubjectUserName\"+:\"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user\"+:\"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| added_regex_field | dest_host |  | ['"hostname\"+:\"+({dest_host}({host}[\w\-.]+))', 'exa_json_path=$..hostname,exa_regex=^({dest_host}({host}[\w\-.]+))$', 'exa_json_path=$.host.hostname,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| added_regex_field | src_domain |  | ['"+SubjectDomainName\"+:\"+({src_domain}({domain}[^\"]+))'] |
| added_regex_field | src_user |  | ['"+SubjectUserName\"+:\"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', '"user\"+:\"+(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))', 'exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| removed_attribute | DupFields |  | N/A |