# Code Changes for microsoft-evsecurity-json-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'dest_host', 'dest_user', 'event_name', 'host', 'src_ip', 'src_port', 'src_user', 'user', 'user_upn'] |
| edit_regex_field | host |  | ['exa_json_path=$..computer_name,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| edit_regex_field | user |  | ['exa_json_path=$..TargetUserName,exa_regex=^(-|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))$'] |
| edit_regex_field | user_upn |  | ['exa_json_path=$..TargetUserName,exa_regex=^(-|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))$'] |
| added_regex_field | dest_host |  | ['exa_json_path=$..computer_name,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| added_regex_field | dest_user |  | ['exa_json_path=$..TargetUserName,exa_regex=^(-|(({user_upn}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\'\]\s"\\,\|]+)?)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))$'] |
| removed_attribute | DupFields |  | N/A |