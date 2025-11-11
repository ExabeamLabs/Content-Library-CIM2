# Code Changes for cisco-asa-str-file-success-client (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'dest_ip', 'dest_port', 'direction', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'policy_name', 'protocol', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | file_dir |  | ['FileName:\s*(|({file_path}(|({file_dir}[^\",]*?))[\\\/]*({src_file_name}({file_name}[^\\\/\",]+?(\.({src_file_ext}({file_ext}[^\\\/\.\s\",]+))))?)))\s*,'] |
| edit_regex_field | file_ext |  | ['FileName:\s*(|({file_path}(|({file_dir}[^\",]*?))[\\\/]*({src_file_name}({file_name}[^\\\/\",]+?(\.({src_file_ext}({file_ext}[^\\\/\.\s\",]+))))?)))\s*,'] |
| edit_regex_field | file_name |  | ['FileName:\s*(|({file_path}(|({file_dir}[^\",]*?))[\\\/]*({src_file_name}({file_name}[^\\\/\",]+?(\.({src_file_ext}({file_ext}[^\\\/\.\s\",]+))))?)))\s*,'] |
| edit_regex_field | file_path |  | ['FileName:\s*(|({file_path}(|({file_dir}[^\",]*?))[\\\/]*({src_file_name}({file_name}[^\\\/\",]+?(\.({src_file_ext}({file_ext}[^\\\/\.\s\",]+))))?)))\s*,'] |
| added_regex_field | src_file_ext |  | ['FileName:\s*(|({file_path}(|({file_dir}[^\",]*?))[\\\/]*({src_file_name}({file_name}[^\\\/\",]+?(\.({src_file_ext}({file_ext}[^\\\/\.\s\",]+))))?)))\s*,'] |
| added_regex_field | src_file_name |  | ['FileName:\s*(|({file_path}(|({file_dir}[^\",]*?))[\\\/]*({src_file_name}({file_name}[^\\\/\",]+?(\.({src_file_ext}({file_ext}[^\\\/\.\s\",]+))))?)))\s*,'] |
| removed_attribute | DupFields |  | N/A |