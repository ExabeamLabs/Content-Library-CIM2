# Code Changes for ibm-hclnotes-str-file-download-success-pulling (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['file_dir', 'file_ext', 'file_name', 'src_file_ext', 'src_file_name', 'src_file_path', 'time'] |
| edit_regex_field | file_dir |  | ['from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*'] |
| edit_regex_field | src_file_ext |  | ['from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*'] |
| edit_regex_field | src_file_name |  | ['from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*'] |
| edit_regex_field | src_file_path |  | ['from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*'] |
| added_regex_field | file_ext |  | ['from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*'] |
| added_regex_field | file_name |  | ['from\s*({src_file_path}(({file_dir}[^\"]+)[\\\/]+)?(({file_name}({src_file_name}[^"]+(\.({file_ext}({src_file_ext}[^\.\"]+)))))))\"*'] |
| removed_attribute | DupFields |  | N/A |