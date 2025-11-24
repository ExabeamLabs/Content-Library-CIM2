# Code Changes for egnyte-e-cef-file-success-fileactivity (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'file_dir', 'file_ext', 'file_name', 'full_name', 'object', 'operation', 'service_name', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | file_dir |  | ['"file/folder":"({src_file_path}({file_dir}[^"]*?[\\\/]+)({file_name}({src_file_name}[^"\\\/]+?(\.({file_ext}({src_file_ext}[^"\.\\\/]+)))?)))\s*"'] |
| edit_regex_field | src_file_ext |  | ['"file/folder":"({src_file_path}({file_dir}[^"]*?[\\\/]+)({file_name}({src_file_name}[^"\\\/]+?(\.({file_ext}({src_file_ext}[^"\.\\\/]+)))?)))\s*"'] |
| edit_regex_field | src_file_name |  | ['"file/folder":"({src_file_path}({file_dir}[^"]*?[\\\/]+)({file_name}({src_file_name}[^"\\\/]+?(\.({file_ext}({src_file_ext}[^"\.\\\/]+)))?)))\s*"'] |
| edit_regex_field | src_file_path |  | ['"file/folder":"({src_file_path}({file_dir}[^"]*?[\\\/]+)({file_name}({src_file_name}[^"\\\/]+?(\.({file_ext}({src_file_ext}[^"\.\\\/]+)))?)))\s*"'] |
| added_regex_field | file_ext |  | ['"file/folder":"({src_file_path}({file_dir}[^"]*?[\\\/]+)({file_name}({src_file_name}[^"\\\/]+?(\.({file_ext}({src_file_ext}[^"\.\\\/]+)))?)))\s*"'] |
| added_regex_field | file_name |  | ['"file/folder":"({src_file_path}({file_dir}[^"]*?[\\\/]+)({file_name}({src_file_name}[^"\\\/]+?(\.({file_ext}({src_file_ext}[^"\.\\\/]+)))?)))\s*"'] |
| removed_attribute | DupFields |  | N/A |