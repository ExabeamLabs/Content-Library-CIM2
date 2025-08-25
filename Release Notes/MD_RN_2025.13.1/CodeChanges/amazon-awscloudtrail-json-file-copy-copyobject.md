# Code Changes for amazon-awscloudtrail-json-file-copy-copyobject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_file_dir |  | ['exa_json_path=$.requestParameters.x-amz-copy-source,exa_regex=^({src_file_path}(({src_file_dir}[^\"]+)[\\\/]+)?(({src_file_name}[^"]+(\.({src_file_ext}[^\.\"]+))?)))$'] |
| edit_regex_field | src_file_ext |  | ['exa_json_path=$.requestParameters.x-amz-copy-source,exa_regex=^({src_file_path}(({src_file_dir}[^\"]+)[\\\/]+)?(({src_file_name}[^"]+(\.({src_file_ext}[^\.\"]+))?)))$'] |
| edit_regex_field | src_file_name |  | ['exa_json_path=$.requestParameters.x-amz-copy-source,exa_regex=^({src_file_path}(({src_file_dir}[^\"]+)[\\\/]+)?(({src_file_name}[^"]+(\.({src_file_ext}[^\.\"]+))?)))$'] |
| edit_regex_field | src_file_path |  | ['exa_json_path=$.requestParameters.x-amz-copy-source,exa_regex=^({src_file_path}(({src_file_dir}[^\"]+)[\\\/]+)?(({src_file_name}[^"]+(\.({src_file_ext}[^\.\"]+))?)))$'] |