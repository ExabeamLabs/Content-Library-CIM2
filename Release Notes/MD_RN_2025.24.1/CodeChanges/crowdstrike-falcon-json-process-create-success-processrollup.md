# Code Changes for crowdstrike-falcon-json-process-create-success-processrollup (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'aid', 'aip', 'cid', 'client', 'container_id', 'dest_host', 'dest_ip', 'dest_port', 'dest_process_command_line', 'dest_process_dir', 'dest_process_name', 'dest_process_path', 'domain', 'email_address', 'email_domain', 'event_code', 'event_name', 'file_name', 'grandparent_process_name', 'group_id', 'hash_md5', 'hash_sha256', 'log_severity', 'os', 'parent_process_id', 'parent_process_name', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_integrity', 'process_name', 'process_path', 'thread_id', 'time', 'user', 'user_sid', 'web_content_type'] |
| removed_regex_field | src_host |  | [] |
| removed_regex_field | src_ip |  | [] |
| removed_regex_field | src_port |  | [] |
| added_regex_field | dest_host |  | ['"ComputerName":"({dest_host}[^"]+)"'] |
| added_regex_field | dest_ip |  | ['"aip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', 'exa_json_path=$..aip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |
| added_regex_field | dest_port |  | ['"aip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?', 'exa_json_path=$..aip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?'] |