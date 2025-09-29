# Code Changes for zeek-z-json-file-success-sbmfiles (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_ip', 'dest_port', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'share_path', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | file_dir |  | ['"name":"({file_path}(({file_dir}[^\"]+?)[\\\/]+?)?({file_name}[^"\\\/]+?(\.({file_ext}[^\.\"\\\/]+))?)?)\\?"'] |
| removed_regex_field | src_file_ext |  | [] |
| removed_regex_field | src_file_name |  | [] |
| removed_regex_field | src_file_path |  | [] |
| added_regex_field | file_ext |  | ['"name":"({file_path}(({file_dir}[^\"]+?)[\\\/]+?)?({file_name}[^"\\\/]+?(\.({file_ext}[^\.\"\\\/]+))?)?)\\?"'] |
| added_regex_field | file_name |  | ['"name":"({file_path}(({file_dir}[^\"]+?)[\\\/]+?)?({file_name}[^"\\\/]+?(\.({file_ext}[^\.\"\\\/]+))?)?)\\?"'] |
| added_regex_field | file_path |  | ['"name":"({file_path}(({file_dir}[^\"]+?)[\\\/]+?)?({file_name}[^"\\\/]+?(\.({file_ext}[^\.\"\\\/]+))?)?)\\?"'] |