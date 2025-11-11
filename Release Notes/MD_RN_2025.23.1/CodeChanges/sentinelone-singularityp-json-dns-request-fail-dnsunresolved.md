# Code Changes for sentinelone-singularityp-json-dns-request-fail-dnsunresolved (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'additional_info', 'dest_domain', 'dest_host', 'dest_user', 'dest_user_full_name', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'host_type', 'os', 'parent_process_dir', 'parent_process_name', 'parent_process_path', 'process_command_line', 'process_dir', 'process_id', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | Platform |  | ['MacOS', 'SentinelOne', 'Unix', 'Windows'] |