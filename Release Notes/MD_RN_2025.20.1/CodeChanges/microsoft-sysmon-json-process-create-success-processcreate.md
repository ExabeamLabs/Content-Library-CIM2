# Code Changes for microsoft-sysmon-json-process-create-success-processcreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'file_ext', 'hash_md5', 'hash_sha256', 'host', 'login_id', 'logon_guid', 'opcode', 'parent_process_command_line', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'provider_guid', 'task_name', 'time', 'user', 'user_sid'] |
| edit_regex_field | process_guid |  | ['"*ProcessGuid"*:"*({process_guid}[^"\s\}]+)'] |
| added_regex_field | additional_info |  | ['"Description":\s*"({additional_info}[^"]+)"'] |
| added_regex_field | parent_process_id |  | ['"ParentProcessId\":\s*\"({parent_process_id}[^\"]+)'] |
| added_regex_field | user_sid |  | ['"UserID\":\s*\"({user_sid}[^\"]+)'] |