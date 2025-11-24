# Code Changes for infoblox-bddi-str-file-write-success-backupsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_host', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'process_id', 'process_name', 'src_ip', 'src_port'] |
| edit_regex_field | additional_info |  | ['\d\d:\d\d:\d\d\s+({dest_host}({host}[\w.-]+))\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?\s+({additional_info}[^~]+?)\s*$'] |
| edit_regex_field | host |  | ['\d\d:\d\d:\d\d\s+({dest_host}({host}[\w.-]+))\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?\s+({additional_info}[^~]+?)\s*$'] |
| edit_regex_field | src_ip |  | ['\d\d:\d\d:\d\d\s+({dest_host}({host}[\w.-]+))\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?\s+({additional_info}[^~]+?)\s*$'] |
| edit_regex_field | src_port |  | ['\d\d:\d\d:\d\d\s+({dest_host}({host}[\w.-]+))\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?\s+({additional_info}[^~]+?)\s*$'] |
| added_regex_field | dest_host |  | ['\d\d:\d\d:\d\d\s+({dest_host}({host}[\w.-]+))\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})?)(:({src_port}\d+))?\s+({additional_info}[^~]+?)\s*$'] |
| removed_attribute | DupFields |  | N/A |