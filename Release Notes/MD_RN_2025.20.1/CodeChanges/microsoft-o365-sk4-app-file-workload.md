# Code Changes for microsoft-o365-sk4-app-file-workload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"DeviceName":"(::ffff:)?({host}[\w\-.]+)"', 'exa_json_path=$..DeviceName,exa_regex=^({host}[\w\-.]+)$'] |