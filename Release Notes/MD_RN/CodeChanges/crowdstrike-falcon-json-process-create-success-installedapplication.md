# Code Changes for crowdstrike-falcon-json-process-create-success-installedapplication (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['account_name', 'aid', 'dest_ip', 'dest_port', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha256', 'old_hash', 'os', 'parent_process_id', 'process_command_line', 'process_id', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] | ['account_name', 'aid', 'dest_ip', 'dest_port', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'hash_md5', 'hash_sha256', 'old_hash', 'os', 'parent_process_id', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| added_regex_field | process_dir | [] | ['exa_regex="TargetImageFileName":\s*"[\\\?]*(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))"'] |
| added_regex_field | process_name | [] | ['exa_regex="TargetImageFileName":\s*"[\\\?]*(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))"'] |
| added_regex_field | process_path | [] | ['exa_regex="TargetImageFileName":\s*"[\\\?]*(|({process_path}({process_dir}[^"]*?)(\\+({process_name}[^"\\]+?))?))"'] |