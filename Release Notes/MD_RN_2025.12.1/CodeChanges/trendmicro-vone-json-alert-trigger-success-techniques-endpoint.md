# Code Changes for trendmicro-vone-json-alert-trigger-success-techniques-endpoint (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['src_host'] | ['process_dir', 'process_name', 'process_path', 'src_host'] |
| added_regex_field | process_dir | [] | ["exa_json_path=$..highlightedObjects[?(@.field == 'processName')].value,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$"] |
| added_regex_field | process_name | [] | ["exa_json_path=$..highlightedObjects[?(@.field == 'processName')].value,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$"] |
| added_regex_field | process_path | [] | ["exa_json_path=$..highlightedObjects[?(@.field == 'processName')].value,exa_regex=^({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?))$"] |