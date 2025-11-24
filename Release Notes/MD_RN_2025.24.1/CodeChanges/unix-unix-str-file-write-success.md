# Code Changes for unix-unix-str-file-write-success (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'process_id', 'process_name', 'src_file_dir', 'src_file_name'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d ({dest_host}({host}[^\s]+)) sftp-server\['] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d ({dest_host}({host}[^\s]+)) sftp-server\['] |
| removed_attribute | DupFields |  | N/A |