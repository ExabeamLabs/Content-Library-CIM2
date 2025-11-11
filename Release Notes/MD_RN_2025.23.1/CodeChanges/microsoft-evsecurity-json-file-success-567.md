# Code Changes for microsoft-evsecurity-json-file-success-567 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'dest_host', 'dest_ip', 'dest_port', 'event_code', 'event_name', 'file_dir', 'file_type', 'host', 'src_file_ext', 'src_file_name', 'src_file_path', 'time', 'user'] |
| edit_regex_field | host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)\s*,\s*({dest_host}({host}[\w\-.]+))', 'Audit\s*({dest_host}({host}[\w\-.]+?))\s+Object Access', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)'] |
| added_regex_field | dest_host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)\s*,\s*({dest_host}({host}[\w\-.]+))', 'Audit\s*({dest_host}({host}[\w\-.]+?))\s+Object Access', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)'] |
| removed_attribute | DupFields |  | N/A |