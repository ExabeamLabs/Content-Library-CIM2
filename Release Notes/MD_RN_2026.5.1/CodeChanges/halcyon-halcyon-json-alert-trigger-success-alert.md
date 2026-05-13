# Code Changes for halcyon-halcyon-json-alert-trigger-success-alert (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"action":', '"dataType":"Alert"', '"id":', '"kind":'] |
| changed_parsed_fields | N/A |  | ['file_dir', 'file_ext', 'file_name', 'file_path'] |
| added_regex_field | file_dir |  | ['exa_json_path=$.process.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))', 'exa_json_path=$.summary.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |
| added_regex_field | file_ext |  | ['exa_json_path=$.process.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))', 'exa_json_path=$.summary.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |
| added_regex_field | file_name |  | ['exa_json_path=$.process.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))', 'exa_json_path=$.summary.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |
| added_regex_field | file_path |  | ['exa_json_path=$.process.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))', 'exa_json_path=$.summary.artifact.filePath,exa_regex=({file_path}({file_dir}[^"]+[\\]+)?({file_name}[^"]+(\.({file_ext}[^"]+))))'] |