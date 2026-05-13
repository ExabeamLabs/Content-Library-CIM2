# Code Changes for microsoft-windows-kv-process-create-success-started (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'event_code', 'event_name', 'host', 'process_command_line', 'process_dir', 'process_name', 'process_path', 'time'] |
| added_regex_field | channel |  | ['"Channel"+:"+({channel}[^"]+)"', 'Channel="({channel}[^"]+)'] |