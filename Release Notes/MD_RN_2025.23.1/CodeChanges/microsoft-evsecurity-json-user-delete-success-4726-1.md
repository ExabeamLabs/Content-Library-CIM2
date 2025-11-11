# Code Changes for microsoft-evsecurity-json-user-delete-success-4726-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'dest_user', 'event_name', 'host', 'src_user', 'user'] |
| edit_regex_field | dest_user |  | ['exa_json_path=$.TargetUserName,exa_regex=^({account_name}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| edit_regex_field | user |  | ['exa_json_path=$.SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | account_name |  | ['exa_json_path=$.TargetUserName,exa_regex=^({account_name}({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$.SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| removed_attribute | DupFields |  | N/A |