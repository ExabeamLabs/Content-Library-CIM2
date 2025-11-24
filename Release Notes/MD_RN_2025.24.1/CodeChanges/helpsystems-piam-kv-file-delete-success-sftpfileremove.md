# Code Changes for helpsystems-piam-kv-file-delete-success-sftpfileremove (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+sftp - sshftl_remove_ok'] |
| added_regex_field | dest_host |  | ['\d\dZ\s+({dest_host}({host}[\w\-.]+))\s+sftp - sshftl_remove_ok'] |
| removed_attribute | DupFields |  | N/A |