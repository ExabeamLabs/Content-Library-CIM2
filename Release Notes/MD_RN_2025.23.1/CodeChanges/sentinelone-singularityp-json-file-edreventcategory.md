# Code Changes for sentinelone-singularityp-json-file-edreventcategory (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_full_name', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'host_type', 'os', 'process_command_line', 'process_id', 'process_name', 'time', 'user'] |
| edit_regex_field | host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |