# Code Changes for microsoft-evsecurity-json-file-success-567-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'user'] |
| edit_regex_field | host |  | ['exa_json_path=$.computer_name,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| added_regex_field | dest_host |  | ['exa_json_path=$.computer_name,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| removed_attribute | DupFields |  | N/A |