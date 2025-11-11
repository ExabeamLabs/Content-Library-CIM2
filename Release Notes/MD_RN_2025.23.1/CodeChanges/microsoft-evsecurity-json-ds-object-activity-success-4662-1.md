# Code Changes for microsoft-evsecurity-json-ds-object-activity-success-4662-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'event_name', 'host', 'src_user', 'time', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$..SubjectUserName,exa_regex=^(SYSTEM|-|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))$'] |
| removed_attribute | DupFields |  | N/A |