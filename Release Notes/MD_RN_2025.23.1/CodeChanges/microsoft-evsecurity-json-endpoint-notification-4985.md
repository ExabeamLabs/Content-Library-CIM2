# Code Changes for microsoft-evsecurity-json-endpoint-notification-4985 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'host', 'process_dir', 'process_name', 'process_path', 'src_user', 'time', 'user'] |
| edit_regex_field | host |  | ['exa_json_path=$.Hostname,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | dest_host |  | ['exa_json_path=$.Hostname,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| removed_attribute | DupFields |  | N/A |