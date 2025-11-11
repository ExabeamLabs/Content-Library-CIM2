# Code Changes for microsoft-sysmon-json-file-stream-create-15 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'log_name', 'process_dir', 'process_name', 'process_path', 'severity', 'target', 'time', 'user', 'user_sid'] |
| edit_regex_field | file_dir |  | ['"TargetFilename":"({target}({file_path}({file_dir}[^"]*?)(\\+({file_name}[^"\\]+?(\.({file_ext}[^"\\\.\s]+))?))))"'] |
| edit_regex_field | file_ext |  | ['"TargetFilename":"({target}({file_path}({file_dir}[^"]*?)(\\+({file_name}[^"\\]+?(\.({file_ext}[^"\\\.\s]+))?))))"'] |
| edit_regex_field | file_name |  | ['"TargetFilename":"({target}({file_path}({file_dir}[^"]*?)(\\+({file_name}[^"\\]+?(\.({file_ext}[^"\\\.\s]+))?))))"'] |
| edit_regex_field | file_path |  | ['"TargetFilename":"({target}({file_path}({file_dir}[^"]*?)(\\+({file_name}[^"\\]+?(\.({file_ext}[^"\\\.\s]+))?))))"'] |
| edit_regex_field | host |  | ['"Hostname":"({dest_host}({host}[^"]+))"'] |
| added_regex_field | dest_host |  | ['"Hostname":"({dest_host}({host}[^"]+))"'] |
| added_regex_field | target |  | ['"TargetFilename":"({target}({file_path}({file_dir}[^"]*?)(\\+({file_name}[^"\\]+?(\.({file_ext}[^"\\\.\s]+))?))))"'] |
| removed_attribute | DupFields |  | N/A |