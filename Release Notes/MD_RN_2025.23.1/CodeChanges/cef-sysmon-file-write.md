# Code Changes for cef-sysmon-file-write (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'object', 'operation', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'result', 'time', 'user'] |
| edit_regex_field | host |  | ['({dest_host}({host}\S+)) CEF:', '\Wdvc=({dest_host}({host}[A-Fa-f:\d]+))', '\Wdvchost=({dest_host}({host}[\w\-.]+))'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}\S+)) CEF:', '\Wdvc=({dest_host}({host}[A-Fa-f:\d]+))', '\Wdvchost=({dest_host}({host}[\w\-.]+))'] |
| removed_attribute | DupFields |  | N/A |