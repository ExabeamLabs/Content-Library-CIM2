# Code Changes for microsoft-defenderep-sk4-process-create-success-processcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'dest_host', 'dest_ip', 'dest_port', 'device_id', 'direction', 'domain', 'event_hub_name', 'event_hub_namespace', 'event_name', 'hash_md5', 'hash_sha1', 'hash_sha256', 'host', 'operation', 'parent_process_command_line', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_id', 'process_integrity', 'process_name', 'process_path', 'product_name', 'protocol', 'result', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_sid', 'web_domain'] |
| edit_regex_field | parent_process_dir |  | ['"InitiatingProcessFolderPath"+:\s*"+({parent_process_path}({parent_process_dir}[^"]*?[\\\/]+)?({parent_process_name}[^"\\\/]+?))"'] |
| edit_regex_field | parent_process_name |  | ['"InitiatingProcessFolderPath"+:\s*"+({parent_process_path}({parent_process_dir}[^"]*?[\\\/]+)?({parent_process_name}[^"\\\/]+?))"', 'InitiatingProcessFileName\\?"+:\s*\\?"+({parent_process_name}[^"\\\/]+?)\\?"'] |
| edit_regex_field | parent_process_path |  | ['"InitiatingProcessFolderPath"+:\s*"+({parent_process_path}({parent_process_dir}[^"]*?[\\\/]+)?({parent_process_name}[^"\\\/]+?))"'] |
| edit_regex_field | process_command_line |  | ['"ProcessCommandLine\\?"+:\s*\\?"\s*({process_command_line}.+?)\s*\\*","'] |
| edit_regex_field | process_dir |  | ['"FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"'] |
| edit_regex_field | process_name |  | ['"FileName\\?"+:\s*\\?"+({process_name}[^"]+?)\\?,"', '"FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"'] |
| edit_regex_field | process_path |  | ['"FolderPath"+:"+({process_path}({process_dir}(\w:)?(?:[^:\]]+)?[\\\/])?({process_name}[^\\\/"\]]+?))"'] |
| added_regex_field | parent_process_command_line |  | ['\"InitiatingProcessCommandLine\\?\"+:\s*\\?\"\s*({parent_process_command_line}.+?)\s*\\*","\w+":'] |