# Code Changes for sentinelone-singularityp-json-file-delete-success-filedelete (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'dest_port', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'user'] |
| added_regex_field | file_dir |  | ['exa_json_path=$.sourceProcessInfo.filePath,exa_regex=^(({file_path}({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.([a-zA-Z]+))))|({=file_dir}[^"]+))', 'exa_json_path=$.targetProcessInfo.tgtFilePath,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |
| added_regex_field | file_ext |  | ['exa_json_path=$.targetProcessInfo.tgtFilePath,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |
| added_regex_field | file_name |  | ['exa_json_path=$.sourceProcessInfo.filePath,exa_regex=^(({file_path}({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.([a-zA-Z]+))))|({=file_dir}[^"]+))', 'exa_json_path=$.targetProcessInfo.tgtFilePath,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |
| added_regex_field | file_path |  | ['exa_json_path=$.sourceProcessInfo.filePath,exa_regex=^(({file_path}({file_dir}[^"]+?[\\\/]+)({file_name}[^"\\\/]+(\.([a-zA-Z]+))))|({=file_dir}[^"]+))', 'exa_json_path=$.targetProcessInfo.tgtFilePath,exa_regex=({file_path}({file_dir}[^"]+[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}\w+))?))$'] |