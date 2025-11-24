# Code Changes for ftp-f-str-file-delete-success-200 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'result', 'src_ip', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\.-]+))\s+(\S+\s+){2}\[\d+\]'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\.-]+))\s+(\S+\s+){2}\[\d+\]'] |
| removed_attribute | DupFields |  | N/A |