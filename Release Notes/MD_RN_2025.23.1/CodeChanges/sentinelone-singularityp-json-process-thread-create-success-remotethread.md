# Code Changes for sentinelone-singularityp-json-process-thread-create-success-remotethread (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_domain', 'dest_host', 'dest_user', 'dest_user_full_name', 'domain', 'event_name', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'os', 'process_dir', 'process_name', 'process_path', 'time', 'user'] |
| edit_regex_field | host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |
| added_regex_field | dest_host |  | ['"endpoint\.name":"({dest_host}({host}[^"]+))'] |