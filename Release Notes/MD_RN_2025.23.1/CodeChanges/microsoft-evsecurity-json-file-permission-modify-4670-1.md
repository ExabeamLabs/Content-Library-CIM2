# Code Changes for microsoft-evsecurity-json-file-permission-modify-4670-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'object_name', 'process_dir', 'process_name', 'process_path', 'src_user', 'time', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| removed_attribute | DupFields |  | N/A |