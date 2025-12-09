# Code Changes for microsoft-evsecurity-xml-endpoint-notification-5890 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>'] |
| edit_regex_field | process_name |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>', '<Message>Process (\'|")?(-|({process_name}[^\s\'"]+))'] |
| edit_regex_field | process_path |  | ['<Data Name(\\)?=(\'|")ProcessName(\'|")>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>'] |