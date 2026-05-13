# Code Changes for microsoft-evsecurity-cef-share-access-5145 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | file_dir |  | ['\Wad\.RelativeTargetName=({file_dir}(?:[^"=]+)?[\\\/])?({file_name}[^=\\:"]+?(\.\s*({file_ext}[^="\\.]+?))?)(\s+(\w+|\w+\.\w+)=|\s*$)'] |
| edit_regex_field | file_ext |  | ['\Wad\.RelativeTargetName=({file_dir}(?:[^"=]+)?[\\\/])?({file_name}[^=\\:"]+?(\.\s*({file_ext}[^="\\.]+?))?)(\s+(\w+|\w+\.\w+)=|\s*$)'] |
| edit_regex_field | file_name |  | ['\Wad\.RelativeTargetName=({file_dir}(?:[^"=]+)?[\\\/])?({file_name}[^=\\:"]+?(\.\s*({file_ext}[^="\\.]+?))?)(\s+(\w+|\w+\.\w+)=|\s*$)'] |