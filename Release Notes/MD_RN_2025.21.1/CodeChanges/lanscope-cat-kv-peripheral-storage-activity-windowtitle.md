# Code Changes for lanscope-cat-kv-peripheral-storage-activity-windowtitle (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'bytes', 'dest_host', 'device_id', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'process_name', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | operation |  | ['\sEvent="({access}({operation}[^"]+))'] |
| added_regex_field | access |  | ['\sEvent="({access}({operation}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |