# Code Changes for microsoft-evsecurity-xml-process-create-success-4688 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_process_dir', 'dest_process_name', 'dest_process_path', 'dest_user', 'domain', 'event_code', 'event_name', 'full_name', 'host', 'login_id', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'service_name', 'src_domain', 'src_host', 'src_user', 'time', 'user', 'user_sid'] |
| edit_regex_field | domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+?)))<'] |
| edit_regex_field | parent_process_guid |  | ['<Data Name(\\)?=(\'|")ProcessId(\'|")>({parent_process_id}({parent_process_guid}[x\da-f]+))<'] |
| edit_regex_field | parent_process_id |  | ['<Data Name(\\)?=(\'|")NewProcessId(\'|")>({parent_process_id}[^<]+)<', '<Data Name(\\)?=(\'|")ProcessId(\'|")>({parent_process_id}({parent_process_guid}[x\da-f]+))<'] |
| edit_regex_field | process_guid |  | ['<Data Name(\\)?=(\'|")NewProcessId(\'|")>({process_id}({process_guid}[x\da-f]+))<'] |
| edit_regex_field | user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}(LOCAL SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))))<'] |
| added_regex_field | process_id |  | ['<Data Name(\\)?=(\'|")NewProcessId(\'|")>({process_id}({process_guid}[x\da-f]+))<'] |
| added_regex_field | src_domain |  | ['<Data Name(\\)?=(\'|")SubjectDomainName(\'|")>(-|({src_domain}({domain}[^<]+?)))<'] |
| added_regex_field | src_user |  | ['<Data Name(\\)?=(\'|")SubjectUserName(\'|")>(-|({src_user}({user}(LOCAL SERVICE|[\w\.\-\!\#\^\~]{1,40}\$?))))<'] |
| removed_attribute | DupFields |  | N/A |