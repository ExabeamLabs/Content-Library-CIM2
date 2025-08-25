# Code Changes for microsoft-sysmon-xml-dll-load-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_dir |  | ['<Data Name\\*=(\'|")ImageLoaded(\'|")>({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<]+))))<\/Data>'] |
| edit_regex_field | file_ext |  | ['<Data Name\\*=(\'|")ImageLoaded(\'|")>({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<]+))))<\/Data>'] |
| edit_regex_field | file_name |  | ['<Data Name\\*=(\'|")ImageLoaded(\'|")>({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<]+))))<\/Data>'] |
| edit_regex_field | file_path |  | ['<Data Name\\*=(\'|")ImageLoaded(\'|")>({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<]+))))<\/Data>'] |
| edit_regex_field | hash_md5 |  | ['<Data Name\\*=(\'|")Hashes(\'|")>[^<>]*?MD5=({hash_md5}[^,<]+)'] |