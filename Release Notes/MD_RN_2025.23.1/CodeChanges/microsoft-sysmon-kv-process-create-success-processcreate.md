# Code Changes for microsoft-sysmon-kv-process-create-success-processcreate (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['domain', 'event_code', 'hash_md5', 'host', 'integrity', 'login_id', 'operation_type', 'parameter_csproj', 'parameter_dll', 'parameter_exe', 'parameter_hta', 'parameter_sct', 'parameter_xml', 'parent_process_command_line', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_command_line', 'service_name', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['Hostname":"({src_host}({host}[^"]+?))"', '\sComputer(?:Name)?\s*=\s*"?({src_host}({host}[^\s"]+))'] |
| added_regex_field | src_host |  | ['Hostname":"({src_host}({host}[^"]+?))"', '\sComputer(?:Name)?\s*=\s*"?({src_host}({host}[^\s"]+))'] |
| removed_attribute | DupFields |  | N/A |