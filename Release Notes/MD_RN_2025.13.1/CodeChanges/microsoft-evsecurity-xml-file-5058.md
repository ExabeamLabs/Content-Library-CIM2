# Code Changes for microsoft-evsecurity-xml-file-5058 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_dir |  | ['<Data Name=(\'|")KeyFilePath(\'|")>({file_path}({file_dir}[^<]+[\\\/]+)?({file_name}[^<\\\/]+(\.({file_ext}[^\s<\\\/]+))?))<'] |
| edit_regex_field | file_ext |  | ['<Data Name=(\'|")KeyFilePath(\'|")>({file_path}({file_dir}[^<]+[\\\/]+)?({file_name}[^<\\\/]+(\.({file_ext}[^\s<\\\/]+))?))<'] |
| edit_regex_field | file_name |  | ['<Data Name=(\'|")KeyFilePath(\'|")>({file_path}({file_dir}[^<]+[\\\/]+)?({file_name}[^<\\\/]+(\.({file_ext}[^\s<\\\/]+))?))<'] |
| edit_regex_field | file_path |  | ['<Data Name=(\'|")KeyFilePath(\'|")>({file_path}({file_dir}[^<]+[\\\/]+)?({file_name}[^<\\\/]+(\.({file_ext}[^\s<\\\/]+))?))<', 'File Path:\s*({file_path}.+?)\s+Operation:'] |