# Code Changes for microsoft-sysmon-kv-process-create-success-createremotethread (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_process_dir', 'dest_process_id', 'dest_process_name', 'dest_process_path', 'domain', 'event_code', 'host', 'operation_type', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'src_host', 'time', 'user'] |
| edit_regex_field | host |  | ['Hostname":"({src_host}({host}[^"]+?))"', '\sComputer(?:Name)?\s*=\s*"?({src_host}({host}[^\s"]+))'] |
| added_regex_field | src_host |  | ['Hostname":"({src_host}({host}[^"]+?))"', '\sComputer(?:Name)?\s*=\s*"?({src_host}({host}[^\s"]+))'] |
| removed_attribute | DupFields |  | N/A |