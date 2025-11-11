# Code Changes for microsoft-sysmon-cef-file-stream-create-success-streamcreated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category_behavior', 'category_significance', 'dest_host', 'event_code', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'process_dir', 'process_name', 'process_path', 'result', 'severity', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}\S+)) CEF:', '\Wdvc=({dest_host}({host}[A-Fa-f:\d]+))', '\Wdvchost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}\S+)) CEF:', '\Wdvc=({dest_host}({host}[A-Fa-f:\d]+))', '\Wdvchost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |