# Code Changes for microsoft-evsecurity-json-share-access-success-5140-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'event_name', 'host', 'login_id', 'share_name', 'src_ip', 'src_port', 'src_user', 'user'] |
| edit_regex_field | host |  | ['exa_json_path=$.host,exa_regex=^({dest_host}({host}[\w.\-]+))$'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | dest_host |  | ['exa_json_path=$.host,exa_regex=^({dest_host}({host}[\w.\-]+))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| removed_attribute | DupFields |  | N/A |