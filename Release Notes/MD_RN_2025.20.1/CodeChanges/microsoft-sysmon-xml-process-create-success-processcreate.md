# Code Changes for microsoft-sysmon-xml-process-create-success-processcreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | login_id |  | ['<Data Name=(\'|")LogonId(\'|")>({login_id}[^<]+)<'] |
| edit_regex_field | parent_process_command_line |  | ['<Data Name\\*=(\'|")ParentCommandLine(\'|")>(-|({parent_process_command_line}[^<]+))<'] |
| edit_regex_field | parent_process_dir |  | ['<Data Name\\*=(\'|")ParentImage(\'|")>(-|({parent_process_path}(({parent_process_dir}[^<]+)\\)?({parent_process_name}[^<]+?)))<\/Data>'] |
| edit_regex_field | parent_process_name |  | ['<Data Name\\*=(\'|")ParentImage(\'|")>(-|({parent_process_path}(({parent_process_dir}[^<]+)\\)?({parent_process_name}[^<]+?)))<\/Data>'] |
| edit_regex_field | parent_process_path |  | ['<Data Name\\*=(\'|")ParentImage(\'|")>(-|({parent_process_path}(({parent_process_dir}[^<]+)\\)?({parent_process_name}[^<]+?)))<\/Data>'] |