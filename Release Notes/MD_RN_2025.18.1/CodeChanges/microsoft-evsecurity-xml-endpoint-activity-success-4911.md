# Code Changes for microsoft-evsecurity-xml-endpoint-activity-success-4911 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | domain |  | ['<Data Name\\*=(\'|")SubjectDomainName(\'|")>({domain}[^<]+)<\/Data>'] |
| edit_regex_field | file_dir |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({object_type}File)</Data><Data Name\\*=(\'|")ObjectName(\'|")>(-|({file_path}({file_dir}[^<]*?)({file_name}[^<\\\/]+?(\.({file_ext}[^<\\\/\.]+?))?)))<'] |
| edit_regex_field | file_ext |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({object_type}File)</Data><Data Name\\*=(\'|")ObjectName(\'|")>(-|({file_path}({file_dir}[^<]*?)({file_name}[^<\\\/]+?(\.({file_ext}[^<\\\/\.]+?))?)))<'] |
| edit_regex_field | file_name |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({object_type}File)</Data><Data Name\\*=(\'|")ObjectName(\'|")>(-|({file_path}({file_dir}[^<]*?)({file_name}[^<\\\/]+?(\.({file_ext}[^<\\\/\.]+?))?)))<'] |
| edit_regex_field | file_path |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({object_type}File)</Data><Data Name\\*=(\'|")ObjectName(\'|")>(-|({file_path}({file_dir}[^<]*?)({file_name}[^<\\\/]+?(\.({file_ext}[^<\\\/\.]+?))?)))<'] |
| edit_regex_field | login_id |  | ['<Data Name\\*=(\'|")SubjectLogonId(\'|")>({login_id}[^<]+)<\/Data>'] |
| edit_regex_field | new_attribute |  | ['<Data Name\\*=(\'|")NewSd(\'|")>({new_attribute}[^<]+)'] |
| edit_regex_field | object_type |  | ['<Data Name\\*=(\'|")ObjectType(\'|")>({object_type}File)</Data><Data Name\\*=(\'|")ObjectName(\'|")>(-|({file_path}({file_dir}[^<]*?)({file_name}[^<\\\/]+?(\.({file_ext}[^<\\\/\.]+?))?)))<'] |
| edit_regex_field | old_attribute |  | ['<Data Name\\*=(\'|")OldSd(\'|")>({old_attribute}[^<]+)'] |
| edit_regex_field | process_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | thread_id |  | ['<Execution ProcessID\\*=(\'|")({process_id}\d+)(\'|") ThreadID\\*=(\'|")({thread_id}\d+)(\'|")\/>'] |
| edit_regex_field | user |  | ['<Data Name\\*=(\'|")SubjectUserName(\'|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data>'] |
| edit_regex_field | user_sid |  | ['<Data Name\\*=(\'|")SubjectUserSid(\'|")>({user_sid}[^<]+)'] |