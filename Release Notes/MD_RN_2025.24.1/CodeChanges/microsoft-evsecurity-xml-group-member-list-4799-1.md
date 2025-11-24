# Code Changes for microsoft-evsecurity-xml-group-member-list-4799-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['<Data Name(\\)?=(\'|")CallerProcessName(\'|")>(-|({process_path}({process_dir}[^<]*?[\\\/]+)?({process_name}[^<\\\/]+)))<\/Data>'] |
| edit_regex_field | process_name |  | ['<Data Name(\\)?=(\'|")CallerProcessName(\'|")>(-|({process_path}({process_dir}[^<]*?[\\\/]+)?({process_name}[^<\\\/]+)))<\/Data>'] |
| edit_regex_field | process_path |  | ['<Data Name(\\)?=(\'|")CallerProcessName(\'|")>(-|({process_path}({process_dir}[^<]*?[\\\/]+)?({process_name}[^<\\\/]+)))<\/Data>'] |