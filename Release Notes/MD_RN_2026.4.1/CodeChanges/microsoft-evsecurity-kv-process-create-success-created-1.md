# Code Changes for microsoft-evsecurity-kv-process-create-success-created-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'dest_user', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'parameter_csproj', 'parameter_dll', 'parameter_exe', 'parameter_hta', 'parameter_sct', 'parameter_xml', 'parent_process_dir', 'parent_process_guid', 'parent_process_id', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_command_line', 'service_name', 'src_domain', 'src_host', 'src_ip', 'src_user', 'time', 'user'] |
| added_regex_field | channel |  | ['"Channel\\":\\"({channel}[^\\"]+)'] |