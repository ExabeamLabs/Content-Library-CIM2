# Code Changes for json-windows-system-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'process_dir', 'process_name', 'process_path', 'src_user', 'time', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| removed_attribute | DupFields |  | N/A |