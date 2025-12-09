# Code Changes for vmware-carbonblackappctrl-kv-process-create-success-execution (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'dest_ip', 'dest_port', 'domain', 'event_name', 'file_hash', 'file_name', 'file_path', 'host', 'path', 'policy_name', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | process_dir |  | ['\sprocess="+({path}({process_path}(({process_dir}[^"]+)\\({process_name}[^"\s]+))))'] |
| edit_regex_field | process_name |  | ['\sprocess="+({path}({process_path}(({process_dir}[^"]+)\\({process_name}[^"\s]+))))'] |
| edit_regex_field | process_path |  | ['\sprocess="+({path}({process_path}(({process_dir}[^"]+)\\({process_name}[^"\s]+))))'] |
| added_regex_field | path |  | ['\sprocess="+({path}({process_path}(({process_dir}[^"]+)\\({process_name}[^"\s]+))))'] |
| removed_attribute | DupFields |  | N/A |