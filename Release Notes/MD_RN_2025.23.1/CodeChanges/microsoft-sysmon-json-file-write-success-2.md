# Code Changes for microsoft-sysmon-json-file-write-success-2 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation_type', 'path', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['"Hostname":"+({dest_host}({host}[\w\-.]+))'] |
| edit_regex_field | process_name |  | ['"Image"+:"+({path}({process_path}(process_dir}[^"]+)\\+({process_name}[^"]+)))"'] |
| edit_regex_field | process_path |  | ['"Image"+:"+({path}({process_path}(process_dir}[^"]+)\\+({process_name}[^"]+)))"'] |
| added_regex_field | dest_host |  | ['"Hostname":"+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | path |  | ['"Image"+:"+({path}({process_path}(process_dir}[^"]+)\\+({process_name}[^"]+)))"'] |
| removed_attribute | DupFields |  | N/A |