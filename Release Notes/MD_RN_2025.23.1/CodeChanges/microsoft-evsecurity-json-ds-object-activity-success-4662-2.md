# Code Changes for microsoft-evsecurity-json-ds-object-activity-success-4662-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_name', 'host', 'result', 'src_user', 'user'] |
| edit_regex_field | user |  | ['exa_json_path=$.event_data.SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$.event_data.SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| removed_attribute | DupFields |  | N/A |