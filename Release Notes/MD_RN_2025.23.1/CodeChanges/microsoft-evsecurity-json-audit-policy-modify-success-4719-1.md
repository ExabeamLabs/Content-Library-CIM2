# Code Changes for microsoft-evsecurity-json-audit-policy-modify-success-4719-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['audit_category', 'host', 'policy_name', 'src_host', 'src_user', 'sub_category', 'user'] |
| edit_regex_field | host |  | ['exa_json_path=$.computer_name,exa_regex=^({src_host}({host}[\w\-.]+))$'] |
| edit_regex_field | user |  | ['exa_json_path=$.event_data.SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| added_regex_field | src_host |  | ['exa_json_path=$.computer_name,exa_regex=^({src_host}({host}[\w\-.]+))$'] |
| added_regex_field | src_user |  | ['exa_json_path=$.event_data.SubjectUserName,exa_regex=^({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))$'] |
| removed_attribute | DupFields |  | N/A |