# Code Changes for zeek-z-json-file-success-sbmfiles (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_ip', 'dest_port', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'share_path', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | file_dir |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| edit_regex_field | file_ext |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| edit_regex_field | file_name |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| edit_regex_field | file_path |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| added_regex_field | src_file_dir |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| added_regex_field | src_file_ext |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| added_regex_field | src_file_name |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| added_regex_field | src_file_path |  | ['"name":"({src_file_path}({file_path}(({src_file_dir}({file_dir}[^\"]+?))[\\\/]+?)?({src_file_name}({file_name}[^"\\\/]+?(\.({src_file_ext}({file_ext}[^\.\"\\\/]+)))?))?))\\?"'] |
| removed_attribute | DupFields |  | N/A |