# Code Changes for microsoft-o365-sk4-file-write-success-filemodified (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'browser', 'bytes', 'category', 'connection_id', 'email_address', 'email_domain', 'log_source', 'object', 'object_id', 'object_type', 'operation', 'os', 'result', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time'] |
| removed_regex_field | file_dir |  | [] |
| removed_regex_field | file_name |  | [] |
| removed_regex_field | file_path |  | [] |
| removed_regex_field | src_file_path |  | [] |
| added_regex_field | src_file_name |  | [',SourceFileName":"({src_file_name}[^,]+)'] |