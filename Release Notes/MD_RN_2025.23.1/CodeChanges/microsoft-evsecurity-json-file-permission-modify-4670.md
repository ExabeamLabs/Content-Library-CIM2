# Code Changes for microsoft-evsecurity-json-file-permission-modify-4670 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['auth_process', 'event_name', 'host', 'process_dir', 'process_name', 'src_user', 'time', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| removed_attribute | DupFields |  | N/A |