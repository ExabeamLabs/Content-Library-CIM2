# Code Changes for microsoft-evsecurity-json-endpoint-activity-success-4691 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | access |  | ['exa_regex=Accesses:\s*({access}[^"]+?)\s*Access Mask:'] |
| edit_regex_field | domain |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Account Domain:\s+({domain}[^\s]+)', 'exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s'] |
| edit_regex_field | file_dir |  | ['exa_regex=Object Name:\s*({file_path}({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\."]+?))))\s*Process Information:'] |
| edit_regex_field | file_ext |  | ['exa_regex=Object Name:\s*({file_path}({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\."]+?))))\s*Process Information:'] |
| edit_regex_field | file_name |  | ['exa_regex=Object Name:\s*({file_path}({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\."]+?))))\s*Process Information:'] |
| edit_regex_field | file_path |  | ['exa_regex=Object Name:\s*({file_path}({file_dir}(?:[^"]+)?[\\\/])?({file_name}[^\\\/"]+?(\.({file_ext}[^\\\/\."]+?))))\s*Process Information:'] |
| edit_regex_field | login_id |  | ['exa_regex=Logon ID:\s+({login_id}[^\s]+)'] |
| edit_regex_field | object |  | ['exa_regex=Object Name:\s*({object}[^"]+?)\s*Process Information:'] |
| edit_regex_field | operation_type |  | ['exa_regex=Object Type:\s*({operation_type}[^"]+?)\s*Object Name:'] |
| edit_regex_field | user |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s'] |
| edit_regex_field | user_sid |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Subject:\s+Security ID:\s+({user_sid}[^\s]+)'] |