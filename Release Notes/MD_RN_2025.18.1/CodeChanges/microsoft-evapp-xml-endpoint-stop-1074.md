# Code Changes for microsoft-evapp-xml-endpoint-stop-1074 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")param7(\'|")>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | process_dir |  | ['<Data Name\\*=(\'|")param1(\'|")>({process_path}(({process_dir}[^\.]+)?\\)?({process_name}[^<\s]+)?)'] |
| edit_regex_field | process_name |  | ['<Data Name\\*=(\'|")param1(\'|")>({process_path}(({process_dir}[^\.]+)?\\)?({process_name}[^<\s]+)?)'] |
| edit_regex_field | process_path |  | ['<Data Name\\*=(\'|")param1(\'|")>({process_path}(({process_dir}[^\.]+)?\\)?({process_name}[^<\s]+)?)'] |
| edit_regex_field | result_reason |  | ['<Data Name\\*=(\'|")param3(\'|")>({result_reason}[^<]+)</Data>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")param7(\'|")>(({domain}[^\\<]+?)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>'] |
| edit_regex_field | user_sid |  | ['<Security UserID\\*=(\'|")({user_sid}[^<\'"]+)(\'|")/>'] |