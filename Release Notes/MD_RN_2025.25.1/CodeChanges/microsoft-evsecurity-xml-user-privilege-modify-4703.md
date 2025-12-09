# Code Changes for microsoft-evsecurity-xml-user-privilege-modify-4703 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>', 'Process Name:\s*(-|({process_path}({process_dir}(?:[^<=]+)?[\\\/])?({process_name}[^\\\/<:]+?)))[\s\<\>\d]+\s+(.*?)?[\w\s]+:'] |
| edit_regex_field | process_name |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>', '<Message>Process (\'|")?(-|({process_name}[^\s\'"]+))', 'Process Name:\s*(-|({process_path}({process_dir}(?:[^<=]+)?[\\\/])?({process_name}[^\\\/<:]+?)))[\s\<\>\d]+\s+(.*?)?[\w\s]+:'] |
| edit_regex_field | process_path |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>', 'Process Name:\s*(-|({process_path}({process_dir}(?:[^<=]+)?[\\\/])?({process_name}[^\\\/<:]+?)))[\s\<\>\d]+\s+(.*?)?[\w\s]+:'] |