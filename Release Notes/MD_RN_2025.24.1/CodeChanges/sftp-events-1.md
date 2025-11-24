# Code Changes for sftp-events-1 (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_agent'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w\-.]+))\s+sftp-[^",]+"({time}\w+\s+\d+\w+\d+\s+\d\d:\d\d:\d\d)'] |
| edit_regex_field | time |  | ['({dest_host}({host}[\w\-.]+))\s+sftp-[^",]+"({time}\w+\s+\d+\w+\d+\s+\d\d:\d\d:\d\d)'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w\-.]+))\s+sftp-[^",]+"({time}\w+\s+\d+\w+\d+\s+\d\d:\d\d:\d\d)'] |
| removed_attribute | DupFields |  | N/A |