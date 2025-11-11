# Code Changes for microsoft-evsecurity-json-user-password-reset-success-4724-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_user', 'event_name', 'host', 'result', 'src_host', 'src_user', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| removed_attribute | DupFields |  | N/A |