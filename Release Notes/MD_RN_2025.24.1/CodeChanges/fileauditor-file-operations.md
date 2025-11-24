# Code Changes for fileauditor-file-operations (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'src_file_dir', 'src_file_name', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+\-]\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+\-]\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |