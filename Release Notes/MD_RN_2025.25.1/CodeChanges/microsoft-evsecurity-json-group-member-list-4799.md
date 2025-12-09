# Code Changes for microsoft-evsecurity-json-group-member-list-4799 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['"CallerProcessName":"(-|({process_path}({process_dir}[^,"]+?[\\\/]+)?({process_name}[^\\\/\s"]+?)))"'] |
| edit_regex_field | process_name |  | ['"CallerProcessName":"(-|({process_path}({process_dir}[^,"]+?[\\\/]+)?({process_name}[^\\\/\s"]+?)))"'] |
| edit_regex_field | process_path |  | ['"CallerProcessName":"(-|({process_path}({process_dir}[^,"]+?[\\\/]+)?({process_name}[^\\\/\s"]+?)))"'] |