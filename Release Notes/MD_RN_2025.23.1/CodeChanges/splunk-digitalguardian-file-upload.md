# Code Changes for splunk-digitalguardian-file-upload (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'host', 'process_name', 'src_file_dir', 'src_file_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['Computer_Name="([^\/\\"]+[\/\\]+)?({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | dest_host |  | ['Computer_Name="([^\/\\"]+[\/\\]+)?({dest_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |