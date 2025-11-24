# Code Changes for unix-unix-str-ssh-traffic-success-sftpsessionopened (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_name', 'host', 'process_id', 'process_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({dest_host}({host}[\w.\-]+)) \S*sftp'] |
| edit_regex_field | time |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({dest_host}({host}[\w.\-]+)) \S*sftp'] |
| added_regex_field | dest_host |  | ['({time}\w+\s+\d+\s+\d+:\d+:\d+)\s*({dest_host}({host}[\w.\-]+)) \S*sftp'] |
| removed_attribute | DupFields |  | N/A |