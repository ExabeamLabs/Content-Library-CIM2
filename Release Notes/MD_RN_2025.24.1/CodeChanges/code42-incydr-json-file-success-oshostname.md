# Code Changes for code42-incydr-json-file-success-oshostname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'bytes', 'dest_host', 'device_id', 'device_name', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_type', 'hash_md5', 'hash_sha256', 'host', 'log_source', 'mime', 'process_dir', 'process_name', 'process_path', 'requested_app', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_uid'] |
| edit_regex_field | dest_host |  | ['"osHostName"+:\s*"+({device_name}({dest_host}[^"]+))"'] |
| edit_regex_field | file_ext |  | ['"fileCategoryByExtension"+:\s*"+({file_ext}[^"]+)"', '"fileName"+:\s*"+({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))"', 'exa_json_path=$.fileName,exa_regex=({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))$'] |
| edit_regex_field | src_file_ext |  | ['"fileName"+:\s*"+({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))"', 'exa_json_path=$.fileName,exa_regex=({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))$'] |
| edit_regex_field | src_file_name |  | ['"fileName"+:\s*"+({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))"', 'exa_json_path=$.fileName,exa_regex=({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))$'] |
| added_regex_field | device_name |  | ['"osHostName"+:\s*"+({device_name}({dest_host}[^"]+))"'] |
| added_regex_field | file_name |  | ['"fileName"+:\s*"+({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))"', 'exa_json_path=$.fileName,exa_regex=({file_name}({src_file_name}[^"]+?(\.({file_ext}({src_file_ext}[^"\s\.]+)))?))$'] |
| removed_attribute | DupFields |  | N/A |