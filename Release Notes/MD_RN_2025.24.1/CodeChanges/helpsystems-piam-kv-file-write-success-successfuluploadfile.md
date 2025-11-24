# Code Changes for helpsystems-piam-kv-file-write-success-successfuluploadfile (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'file_ext', 'file_name', 'file_path', 'host', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_ext |  | ['Successful upload of file (?:({src_file_dir}(\/[^\/]+)*\/))?({src_file_name}({file_name}[^\/.]+\.?({src_file_ext}({file_ext}[^\/]*)))) from '] |
| edit_regex_field | file_name |  | ['Successful upload of file (?:({src_file_dir}(\/[^\/]+)*\/))?({src_file_name}({file_name}[^\/.]+\.?({src_file_ext}({file_ext}[^\/]*)))) from '] |
| edit_regex_field | host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+(scp|sftp) - sshftl_upload_ok'] |
| edit_regex_field | src_file_dir |  | ['Successful upload of file (?:({src_file_dir}(\/[^\/]+)*\/))?({src_file_name}({file_name}[^\/.]+\.?({src_file_ext}({file_ext}[^\/]*)))) from '] |
| added_regex_field | dest_host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+(scp|sftp) - sshftl_upload_ok'] |
| added_regex_field | src_file_ext |  | ['Successful upload of file (?:({src_file_dir}(\/[^\/]+)*\/))?({src_file_name}({file_name}[^\/.]+\.?({src_file_ext}({file_ext}[^\/]*)))) from '] |
| added_regex_field | src_file_name |  | ['Successful upload of file (?:({src_file_dir}(\/[^\/]+)*\/))?({src_file_name}({file_name}[^\/.]+\.?({src_file_ext}({file_ext}[^\/]*)))) from '] |
| removed_attribute | DupFields |  | N/A |