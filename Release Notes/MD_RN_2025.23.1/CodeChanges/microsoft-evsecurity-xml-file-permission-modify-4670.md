# Code Changes for microsoft-evsecurity-xml-file-permission-modify-4670 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_name |  | ['<Data Name(\\)?=(\\)?("|\')+ObjectName(\\)?("|\')+>(-|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?))|[^\\:<]+)<\/Data>', 'Process:\s*([^$]+?)Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({file_name}({process_name}[^\s\\\/]+)))\s+Permissions Change:'] |
| edit_regex_field | process_dir |  | ['Process:\s*([^$]+?)Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({file_name}({process_name}[^\s\\\/]+)))\s+Permissions Change:'] |
| edit_regex_field | process_name |  | ['Process:\s*([^$]+?)Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({file_name}({process_name}[^\s\\\/]+)))\s+Permissions Change:'] |
| edit_regex_field | process_path |  | ['Process:\s*([^$]+?)Process Name:\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({file_name}({process_name}[^\s\\\/]+)))\s+Permissions Change:'] |
| edit_regex_field | src_user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<'] |
| edit_regex_field | user |  | ['<Data Name=(\'|")SubjectUserName(\'|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))<', 'Subject:\s*([^"]+?)Account Name:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |