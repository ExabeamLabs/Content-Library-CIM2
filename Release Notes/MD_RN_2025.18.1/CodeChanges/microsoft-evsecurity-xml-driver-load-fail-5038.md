# Code Changes for microsoft-evsecurity-xml-driver-load-fail-5038 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['<Data Name\\*=(\'|")param1(\'|")>({additional_info}[^<]+)<'] |
| edit_regex_field | file_dir |  | ['<Data Name\\*=(\'|")param1(\'|")>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)</Data>', '<param1>(-|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?))|[^\\:<]+)<'] |
| edit_regex_field | file_ext |  | ['<Data Name\\*=(\'|")param1(\'|")>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>', '<param1>(-|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?))|[^\\:<]+)<'] |
| edit_regex_field | file_name |  | ['<Data Name\\*=(\'|")param1(\'|")>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>', '<param1>(-|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?))|[^\\:<]+)<'] |
| edit_regex_field | file_path |  | ['<Data Name\\*=(\'|")param1(\'|")>({file_path}[^<]+)</Data>', '<param1>(-|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?))|[^\\:<]+)<'] |
| edit_regex_field | process_id |  | ['ProcessID\\*=(\'|")({process_id}\d+)(\'|")'] |
| edit_regex_field | thread_id |  | ['ThreadID\\*=(\'|")({thread_id}\d+)(\'|")'] |