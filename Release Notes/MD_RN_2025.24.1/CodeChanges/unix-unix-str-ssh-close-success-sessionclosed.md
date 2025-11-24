# Code Changes for unix-unix-str-ssh-close-success-sessionclosed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'host', 'process_id', 'process_name', 'src_ip', 'src_port', 'user'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[^\s]+)) sftp-server\['] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d(\.\S+)? ({dest_host}({host}[^\s]+)) sftp-server\['] |
| removed_attribute | DupFields |  | N/A |