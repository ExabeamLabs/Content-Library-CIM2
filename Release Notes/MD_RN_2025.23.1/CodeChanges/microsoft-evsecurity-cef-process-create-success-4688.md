# Code Changes for microsoft-evsecurity-cef-process-create-success-4688 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'operation_type', 'parent_process_dir', 'parent_process_guid', 'parent_process_name', 'parent_process_path', 'path', 'process_command_line', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'service_name', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['\Wdhost=({src_host}({host}[\w\-\.]+))\s*(\w+=|$)', '\Wdvchost=({src_host}({host}[\w\-\.]+))\s*(\w+=|$)'] |
| edit_regex_field | process_guid |  | ['\Wcs3=({process_id}({process_guid}[^\s]+))\s*(\w+=|$)'] |
| added_regex_field | process_id |  | ['\Wcs3=({process_id}({process_guid}[^\s]+))\s*(\w+=|$)'] |
| added_regex_field | src_host |  | ['\Wdhost=({src_host}({host}[\w\-\.]+))\s*(\w+=|$)', '\Wdvchost=({src_host}({host}[\w\-\.]+))\s*(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |