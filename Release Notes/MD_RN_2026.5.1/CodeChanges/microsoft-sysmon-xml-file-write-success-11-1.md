# Code Changes for microsoft-sysmon-xml-file-write-success-11-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'path', 'process_dir', 'process_guid', 'process_id', 'process_name', 'process_path', 'run_level', 'time', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |