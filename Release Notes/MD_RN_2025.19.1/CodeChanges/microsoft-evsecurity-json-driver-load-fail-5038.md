# Code Changes for microsoft-evsecurity-json-driver-load-fail-5038 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'login_id', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Account Domain:\s+({domain}[^\s]+)', 'exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s'] |
| edit_regex_field | file_dir |  | ['exa_regex=File Name: (|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?))) '] |
| edit_regex_field | file_ext |  | ['exa_regex=File Name: (|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?))) '] |
| edit_regex_field | file_name |  | ['exa_regex=File Name: (|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?))) '] |
| edit_regex_field | file_path |  | ['exa_regex=File Name: (|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?))) '] |
| edit_regex_field | user |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Account Name:\s*(({domain}[^:\\]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+){1,2}:\s'] |
| edit_regex_field | user_sid |  | ['exa_json_path=$.UserID,exa_regex=(({user_sid}S-[^"]+?)|(({domain}[^"]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"', 'exa_regex=Subject:\s+Security ID:\s+({user_sid}[^\s]+)'] |
| added_regex_field | login_id |  | ['exa_regex=Logon ID:\s+({login_id}[^\s]+)'] |