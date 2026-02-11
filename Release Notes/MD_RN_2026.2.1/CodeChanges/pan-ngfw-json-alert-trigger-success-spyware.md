# Code Changes for pan-ngfw-json-alert-trigger-success-spyware (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_name |  | ['exa_json_path=$..FileName,exa_regex=^({file_name}[^"]+?)[\\\/]*$'] |