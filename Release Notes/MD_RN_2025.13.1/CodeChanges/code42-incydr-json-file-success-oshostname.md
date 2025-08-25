# Code Changes for code42-incydr-json-file-success-oshostname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'bytes', 'dest_host', 'device_id', 'domain', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_type', 'hash_md5', 'hash_sha256', 'host', 'log_source', 'mime', 'process_dir', 'process_name', 'process_path', 'requested_app', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'url', 'user', 'user_uid'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['"filePath"+:\s*"+({file_dir}[^"]+)"'] |